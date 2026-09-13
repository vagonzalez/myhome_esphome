pip install esphome esptool

### Compile

```bash
esphome clean your_config.yaml
esphome compile your_config.yaml
```

### Flash

```bash
esptool.py --port /dev/ttyUSB0  --baud 115200 erase_flash
esptool.py --port /dev/ttyUSB0 --chip esp32 --baud 115200 write_flash 0x10000 ./.esphome/build/dormitorio_luz_ventilador/.pioenvs/dormitorio_luz_ventilador/firmware.factory.bin
```

### Windows USB-TTL drivers
- https://github.com/theAmberLion/Prolific/blob/main/PL2303_Prolific_v3.3.2.105.exe

