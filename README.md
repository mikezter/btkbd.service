# btkbd.service
Pairs your Bluetooth keyboard at system start. You can then use it
to log in.

How to install on most systems:
--------------------

Prerequisites:

 * Pair your keyboard the usual way.
 * Find the keyboards MAC address: `echo exit | bluetoothctl`
 * Find the controllers device identifier: `hcitool dev`

Install service files:

```
cp btkbd.conf /etc/
cp btkbd.service /etc/systemd/system
```

Enable the service:

```
systemctl start btkbd
systemctl enable btkbd
```
