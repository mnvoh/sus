## Waybar Config

![Waybar](assets/waybar.png)


### Usage

```
Usage of bin/susw:
  -a    Show amperage instead of wattage
  -c string
        HEX color for critical threshold (default "#ff5555")
  -tc float
        Critical wattage threshold (default 108)
  -tw float
        Warning wattage threshold (default 96)
  -w string
        HEX color for warning threshold (default "#f1fa8c")
```


### Waybar Config

```json
{
  ...
  "custom/astral": {
    "exec": "susw",
    "return-type": "json",
    "interval": 2,
    "format": "{}",
    "tooltip": true
  },
  ...
}
```

## Upstream README

Introduction

  • The 12V-2x6 (12VHPWR) connectors are notorious for their flammability.
  • The ASUS ROG ASTRAL implementation of RTX 5090 monitors voltage and current
    flowing through connector pins.

  This project provides a native Linux implementation of the current monitoring
  functionality of ASUS ROG ASTRAL devices. The support is currently limited to
  ROG-ASTRAL-RTX5090-O32G devices.

  • The bin/susm binary implements a simple monitor.
  • The bin/susd binary implements a simple daemon that attempts to reduce the
    power draw when it detects either overload on any of the connectors pins or
    when there is a significant mismatch between individual wires.


