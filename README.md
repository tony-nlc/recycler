# Recycler
This is a recycler package for demostrating my understanding on Linux for ACIT 2420.

Usage:
```bash
recycler -d <filename>          # This will mv the file to the recycler bin under user's directory
recycler -l                     # This will list all the items inside the bin
recycler -r <unique name>       # This will restore the file back to its original filepath
recycler -e                     # This will empty the recycler bin
```

This package come with two unit files.

```
# Filename: recycler.service
[Unit]
Description=Clean Recycler

[Service]
Type=oneshot
ExecStart=/usr/bin/recycler -e

[Install]
WantedBy=multi-user.target
```

```
# Filename: recycler.timer
[Unit]
Description=Clean Recycler every month

[Timer]
OnCalendar=monthly
Persistent=true

[Install]
WantedBy=timers.target
```