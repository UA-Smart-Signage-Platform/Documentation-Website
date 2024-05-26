## Requirements

- Git
- Docker and Docker Compose
- Mosquitto (the package is called mosquitto in apt)

## Frontend & Backend

1. Clone the Repository
    ```
    git clone https://github.com/UA-Smart-Signage-Platform/Content-Manager-System-and-Content-Creator-Tool && cd Content-Manager-System-and-Content-Creator-Tool
    ```

2. Generate the Mosquitto passwd file (replace with the username and password you wish to use)
    ```
    mosquitto_passwd -b -c mosquitto/passwd BROKER_USERNAME_HERE BROKER_PASSWORD_HERE
    ```

3. (Optional) Change variables in `prod.env` and `docker-compose.prod.yaml`
    - Change `localhost` to the ip address you want to use
    - If you generated the mosquitto passwd file replace the `MQTT_USERNAME` `MQTT_PASSWORD` values in `prod.env` accordingly
    - Change other values as you see fit, for more information visit the [enviroment variables page]()

4. Run the production docker-compose
    ```
    docker-compose -f docker-compose.prod.yaml up --build
    ```

5. You can visit the website at the ip you set at port 3000. The default login is `admin` `admin`.

## Media Player

1. Grab the [linux image]() and write it into your sd card using a tool like [rpi-imager](https://github.com/raspberrypi/rpi-imager)

2. Boot into the OS and wait for the program to open.

3. Follow the instructions on the screen and enter the Hotspot and visit the configuration page

4. Connect to the internet and change the configuration values as you see fit (for more information visit the [config page]())
    - Ways to connect to the Internet:
        - If you plug in an ethernet cable and your network dynamically assigns ip addresses just leave the wifi password input empty and you are good to go.
        - If you want to use wifi choose one of the options available and input the password.
        - If your network requires you to set an static ip, currently there is no way to do it with our program. For this you will need to plug in a mouse and keyboard or set it up by editing the filesystem on the sd card directly. There is an open feature request for this [here](https://github.com/UA-Smart-Signage-Platform/Media-Player/issues/22).

    - Important configuration values:
        - Change the `host` to the ip you set in the configuration for the backend or a different one if you wish to use an external broker.
        - Change the `port` to fit the correct port for the broker (80 is the default for our broker).
        - Change the `username` and `password` to the correct credentials for the broker (see [#2](#frontend-backend)).
        - Change the `transport` to `websockets` if you are using our default configuration in the backend.
        - Change the `name` to the name you want the monitor to show up as in the system. 