# 3D Printer configs

This repository contains my printer configs.

## Printers

- Creality
  - Ender 3 Pro
    - Creality V4.2.7 Board

## Known issues

### Klipper - USB don't show when connecting the printer to Ubuntu

Run the folloing commands should fix the issue.

> brltty is some kind of barile service, its a problem that keeps popping up, grabbing all kinds of USB connections from arduino to printers. I think I rebooted after running the commands too, although it's usually not necessary in linux.

```shell
sudo systemctl stop brltty-udev.service

sudo systemctl mask brltty-udev.service

sudo systemctl stop brltty.service

sudo systemctl disable brltty.service
```
