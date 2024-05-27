### Visual Artifacts in Media Player Window

- This seems to be a problem with the compositor and the command `export WEBKIT_DISABLE_COMPOSITING_MODE=1` seems to fix it.

### Media Player Takes too Long to Start

- This is a problem with GTK applications and can be fixed by uninstalling/stopping the xdg-desktop-portal

### NetworkManager pop-up Upon Wrong Password

- During the user configuration, if a wrong password wifi password is inputted the program expects that the nmcli command will return and will open the Hotspot again. By default NetworkManager opens a pop-up upon receiving an incorrect password, which causes problems with our program. If you are using nm-applet you can deactivate this by running it with `--no-agent`. This is already fixed in the official linux image.

### Running without NetworkManager

- If you want to run the program without the NetworkManager (if you are in WSL for example), firstly generate the config file manually as explained above and remove the `network_manager` import from `media_player.py` and remove all the places that it is used inside the file. This is possible since NetworkManager is only required for the user configuration part of the Media Player. (this works as of **26/05/2024**)


### Cannot find module (Frontend)

- This error happens when the system has not yet installed the requirements;
```
Failed to compile
Error: Cannot find module [module]
```
To fix this simply run:
```
docker-compose up --build
```