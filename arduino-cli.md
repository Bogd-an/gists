# portable arduino-cli

create folder .arduino

download and unzip https://docs.arduino.cc/arduino-cli/installation/#latest-release

arduino-cli.yaml
``` yaml
board_manager:
    additional_urls:
        -
directories:
    data: ./.arduino/arduino-data
    downloads: ./.arduino/arduino-downloads
    user: ./.arduino/arduino-sketchbook
```

arduino-cli.bat
``` bat
@echo off
set "ARDUINO_DIR=%~dp0"
set "ARDUINO_DIR=%ARDUINO_DIR:~0,-1%"
"%ARDUINO_DIR%\arduino-cli.exe" --config-dir "%ARDUINO_DIR%" %*
```

Then add to PATH arduino-cli.bat

``` bash
arduino-cli core update-index
arduino-cli core install arduino:avr
```

