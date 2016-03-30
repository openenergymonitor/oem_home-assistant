
## OpenEnergyMonitor config for Home Assistant

[Home Assistant](https://home-assistant.io/) is an open-source home automation platform running on Python 3.

## Install Home Assistant

Assuming starting with Raspbien Jessie (tested on emonPi image): 

    sudo apt-get install python3-pip
    pip3 install homeassistant

Install and run with custom config location on R/W partition: 

```
mkdir ~/data/home-assistant 
ln -s /home/pi/oem_home-assistant /home/pi/data/home-assistant
hass --config /home/pi/data/home-assistant
```

## Run on boot

```
sudo cp /home/pi/oem_home-assistant/home-assistant@pi.service /lib/systemd/system/home-assistant@pi.service
sudo systemctl --system daemon-reload
sudo systemctl enable home-assistant@pi
sudo systemctl start home-assistant@pi
```

Start with `systemctl start home-assistant@pi.service`

## Optional:

``` 
sudo apt-get install python-Levenshtein
sudo  apt-get install net-tools nmap
```
