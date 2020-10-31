# adsbexchange-stats
ADSB-Exchange Statistics Beta Fork from [ADSB-Exchange](https://github.com/adsbxchange/adsbexchange-stats)

This installer is meant only for RPi running the [The ADS-B Receiver Project](https://github.com/jprochazka/adsb-receiver) image from [jprochazkat](https://github.com/jprochazka) with the inbuilt ADS-B Exchange feeder script.

The ADS-B Exchange feeder script from [The ADS-B Receiver Project](https://github.com/jprochazka/adsb-receiver) must have been installed before.

### Install adsbexchange-stats
```
curl -o /tmp/stats.sh https://raw.githubusercontent.com/amnesica/adsbexchange-stats/master/stats.sh
sudo bash /tmp/stats.sh
```

### Show stats URL on RPi console
```
adsbexchange-showurl
```

### Systemd Status
```
sudo systemctl status adsbexchange-stats
```

### Restart
```
sudo systemctl restart adsbexchange-stats
```

### Figure the URL out yourself
Replace UUID with the adsbx stats generated uuid:
https://www.adsbexchange.com/api/feeders/?feed=UUID

--adsbx-git-discord

### Uninstall

```
sudo bash /usr/local/share/adsbexchange-stats/uninstall.sh
```

For early versions just disable the service:
```
sudo systemctl disable --now adsbexchange-stats
```
