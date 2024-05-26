## Widget Format

The widgets are HTML snippets that are put together to create what is show on the monitors. These widgets can have different variables inside them that have the format `[[VariableName]]`. By default, the system fills in the default variables `Top`, `Left`, `Width`, `Height` and [`widgetID`](#widgetID) meaning that all widgets can use this variables. For example, if our widget looks like this:

```
<div style="top: [[top]]px; left: [[left]]px; width: [[width]]px; height: [[height]]px;">
    <p>Hello [[widgetID]]</p>
</div>
```

in the end result, considering some random values, when the HTML is generated it will look like this

```
<div style="top: 1234px; left: 4321px; width: 200x; height: 200px;">
    <p>Hello 4e8a9f772d734b48bfb52d23def15429</p>
</div>
```

For consistency, all widgets end with the `.widget` extension.

## Widget Location

By default, all widgets are located at `resources/static/widgets/`.

## widgetID

Apart from the position and size variables, each widget can also have a `widgetID` variable. This variable is a 32 character long string containing numbers and letters (it's an uuid without the `-`s). It is specially usefull in situations where you need an id that is different between two of the same widget in the same template. For example, in our media template this is used so that our javascript functions know what divs to target when there is more than 1 media widget on a template:

```
<div style="top: [[top]]px; left: [[left]]px; width: [[width]]px; height: [[height]]px;">
    <video autoplay muted class="stretch" id="video[[widgetID]]"></video>
    <img class="stretch" style="display: none;" id="image[[widgetID]]">
</div>
```

## Adding Variables (aka Content)

![Template Demonstration](../files/template-demo.gif)

```
Image Widget Example

<div style="top: [[top]]px; left: [[left]]px; width: [[width]]px; height: [[height]]px;">
    <img src="[[image]]" class="stretch">
</div>
```

If we want our widget to have extra widgets ([currently only one per widget](#only-one-content-per-widget)) we have to give it what we call extra `Contents`. These contents have a `name`, a `type` and an optional list of `options`. The name is what will be replaced in the widget, in the example above it would be `image`. For the types there are currently 2 supported: `media` and `options`

- The `media` type will allow the user to choose a file or a folder. If a file is chosen the variable will be replaced with the file name, if a folder is chosen it will be replace with `file1.mp4","file2.png` (see [here](#non-scalable-playlist-content-type))

- The `options` type will give the user the option to choose between what is inside the `options` list. This is used, for example, in our temperature widget, where we set the list of options as a list of weather stations for the user to choose from.

```
<div hx-get="http://localhost:5000/ipma/temperature?station=[[station]]" ...</div>
```

## Using External APIs

As we can see in the example above, our temperature widget is fetching information about the temperature. This information is being fetched from the flask instance running in the Media Player. To obtain this information we use htmx in our widget to make a get request to the desired endpoint. If we want to fetch other information from the internet we must first create the endpoint in flask that fetches and parses that information. Another example of a widget that does this is our events widget:

```
<div style="background-color: white; position: absolute; top: [[top]]px; left: [[left]]px; width: [[width]]px; height: [[height]]px; display: flex; flex-direction: column; align-items: center; justify-content: center;">
    <div id="[[widgetID]]-1" style="position: static; text-align: center; margin-bottom: 5vw; width: 95%; color: #000;" hx-get="http://127.0.0.1:5000/ua/events" hx-trigger="load, every 30m">
    </div>
    <div id="[[widgetID]]-2" style="position: static; text-align: center; width: 95%; color: #000;" hx-get="http://127.0.0.1:5000/ua/events" hx-trigger="load, every 30m">
    </div>
</div>
```

where the endpoint looks something like this:

```
@app.route("/ua/events")
def ua_events():
    url = "..."

    # Make Request to the URL
    response = requests.get(url).content
    
    # Parse the Information
    title = event["title"]

    start_datetime = datetime.strptime(event["start_utc_datetime"], "%Y-%m-%d %H:%M:%S")
    start_date =start_datetime.strftime("%d-%m-%Y")
    end_datetime = datetime.strptime(event["end_utc_datetime"], "%Y-%m-%d %H:%M:%S")
    end_date =end_datetime.strftime("%d-%m-%Y")

    # Return the Information
    return f'''
    <p style="font-size: 1.5vw; margin: 0; ">{date}</p>
    <p style="font-size: 1.1vw; margin: 0.1vw 0;">{location}</p>
    <p style="font-size: 1.7vw; font-weight: 600; margin-top: 0.5vw;">{title}</p>
    '''
```

## Font Scaling

The HTML is generated based on the resolution on the monitor, this means that the widgets should not use absolute pixel values for sizes and fonts.

## Adding a Widget

There is currently no easy way to add a widget to the database. There is an [open issue](https://github.com/UA-Smart-Signage-Platform/Content-Manager-System-and-Content-Creator-Tool/issues/154) regarding this. Currently, if we want to add a widget to the database we must add it to the `DataLoader.java` file located at `src/main/java/deti/uas/uasmartsignage/initializer/` inside the `loadTemplates` function. An example of how to do it would be:

```
Widget mediaWidget = new Widget();
mediaWidget.setName("Media");
mediaWidget.setPath("static/widgets/media.widget");
widgetRepository.save(mediaWidget);
Content mediaWidgetContent = new Content();
mediaWidgetContent.setName("videos");
mediaWidgetContent.setType("media");
mediaWidgetContent.setWidget(mediaWidget);
contentRepository.save(mediaWidgetContent);
```

## Current Limitations

### Only One Content per Widget

The way the frontend currently works only one `Content` can be assigned to each widget.

### Non Scalable Media Content Type

Due to how our media widget uses the media content's values, when the user chooses a folder the value of the variable is replaced with `file1.mp4","file2.png` while `file1.mp4,file2.png` would make more sense in general but wouldn't work with the current version of our media widget.

```
var videoList[[widgetID]] = ["[[videos]]"];
```