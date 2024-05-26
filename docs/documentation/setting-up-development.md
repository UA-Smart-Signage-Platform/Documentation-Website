## Requirements

- Git
- Docker and Docker Compose
- python3 and pip
- NetworkManager (see [here](#running-without-networkmanager))

## Frontend & Backend

1. Clone the Repository
    ```
    git clone https://github.com/UA-Smart-Signage-Platform/Content-Manager-System-and-Content-Creator-Tool && cd Content-Manager-System-and-Content-Creator-Tool
    ```

2. (Optional) Change variables in `dev.env`

3. Run the development docker-compose
    ```
    docker-compose -f docker-compose.yaml up --build
    ```

4. You can visit the website at `http://localhost:3000` the default login is `admin` `admin`

## Media Player

1. Clone the Repository
    ```
    git clone https://github.com/UA-Smart-Signage-Platform/Media-Player && cd Media-Player
    ```

2. (Optional, Recommended) Create the config manually (if you don't do this, the program is gonna open an hotspot on startup)
    ```
    cp default_config.ini config.ini
    ```

3. (Optional) Edit the values inside `config.ini`, for more information visit the [config page](../media-player-config/)

4. Follow the instructions in the README (Debian and Debian-based only) or use this one-liner.
    ```
    sudo apt install libgirepository1.0-dev gcc libcairo2-dev pkg-config python3-dev gir1.2-gtk-4.0 python3-gi python3-gi-cairo gir1.2-gtk-3.0 gir1.2-webkit2-4.1 && python3 -m venv venv && source venv/bin/activate && pip install -r requirements.txt
    ```

5. Run the Media Player
    ```
    python3 media_player.py
    ```
