# systemd-oswbb

systemd unit file for Oracle OS Watcher

## Usage

Oracle's OS Watcher is a small utility shipped within TFA. In addition it can
be downloaded as standalone utility using My Oracle Support Note
[301137.1](https://support.oracle.com/epmos/faces/DocumentDisplay?id=301137.1).

Please don't forget to update paths in `oswatcher.service`.

After putting `oswatcher.service` in `/etc/systemd/system` reload systemd using
`systemctl daemon-reload` and enable the unit using
`systemctl enable oswatcher.service`. After that one can start the service as usual
with `systemctl start oswatcher.service`.
