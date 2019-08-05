# systemd-oswbb

systemd unit file for Oracle OS Watcher

## Usage

Oracle's OS Watcher is a small utility shipped within TFA. In addition it can
be downloaded as standalone utility using My Oracle Support Note
[301137.1](https://support.oracle.com/epmos/faces/DocumentDisplay?id=301137.1).

The standalone utility does not contain a start/stop script. To integrate
with systemd use these two files:

1. oswatcher.conf
2. oswatcher.service

`oswatcher.conf` includes all settings needed to run `startOSWbb.sh` using systemd.
Please don't forget to update `oswatcher.service` to reference the location of the
configuration file.

After putting `oswatcher.service` in `/etc/systemd/system` reload systemd using
`systemctl daemon-reload` and enable the unit using
`systemctl enable oswatcher.service`. After the one can start the service as usual
using `systemctl start oswatcher.service`.
