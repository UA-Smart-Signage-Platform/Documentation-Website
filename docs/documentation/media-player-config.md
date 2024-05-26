The configuration can be changed during the setup of the Media Player or it can be changed manually by editing the `config.ini` file.

## MQTT

- `host` - broker ip address
- `port` - broker port
- `keepalive_mqtt` - mqtt client keepalive delay (causes problems if greater or equal to 60)
- `username` - broker username (credentials)
- `password` - broker password (credentials)
- `name` - name that the monitor will appear as in the system
- `register_topic` - topic used to send registration message
- `transport` - mqtt transport method (options are 'tcp' or 'websockets')
- `keepalive_logs_delay` - delay between keepalive log messages (see [message protocol](../message-protocol))
- `keepalive_logs_topic` - topic to send the keepalive log messages

## MediaPlayer

- `default_template` - template to be used when no rule is being displayed
- `savings_mode` - attemt to blank screen when no rule is being displayed (please see [here](#savings-mode) before using it)

## Logging

- `log_file` - file to store the log messages
- `log_level` - [logging level](https://docs.python.org/3/library/logging.html#logging-levels) (options are 'DEBUG', 'INFO', 'WARNING', 'ERROR', 'CRITICAL')

## Savings Mode

If this active, when no rules are being displayed, it calls `xset dpms force off` to blank the screen. This might not work on some screens and it also does not working if the screen blanking is turned off in the raspberry pi. More info [here](https://wiki.archlinux.org/title/Display_Power_Management_Signaling).
