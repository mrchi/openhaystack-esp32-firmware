# openhaystack-esp32-firmware

This is a compiled [OpenHaystack](https://github.com/seemoo-lab/openhaystack) firmware for esp-wroom-32.

Tested on `macOS 12.4`.

## How to use(macOS)

### Install VCP driver

install CP210x USB to UART Bridge VCP Driver for esp-wroom-32

```
brew install silicon-labs-vcp-driver
```

> you may need to run installer.app manually by following prompt of brew command.

### Install OpenHaystack app on Mac

Follow [the instruction from OpenHaystack](https://github.com/seemoo-lab/openhaystack#how-to-use-openhaystack) to install OpenHaystack app on Mac.

### Get advertisement key

1. Open OpenHaystack app on Mac, create a new accessory.
2. Right click the accessory name, choose "Copy advertisement key" -> "Base64".
3. Right click the accessory name, choose "Mark as deployed".

![Alt text](images/Screen%20Shot%202022-11-09%20at%2012.55.12.png)

### Deploy firmware on esp-wroom-32

Connect esp32 with Macos by USB, execute

```
./flash_esp32.sh -p /dev/yourSerialPort "Base64-encoded advertisement key"
```

**You might need to reset your device after running the script before it starts sending advertisements.**

### Get accessory position on OpenHaystack app

![Alt text](images/Screen%20Shot%202022-11-09%20at%2012.59.15.png)

## References

- [seemoo-lab/openhaystack](https://github.com/seemoo-lab/openhaystack)
