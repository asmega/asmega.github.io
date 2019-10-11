---
layout: post
title: Restarting nginx
date: 2011-05-07
---

A quick how to on restarting nginx when init scripts or start scripts aren't available. These aren't added by default as far as I know.

This is done by sending the correct signal to nginx. The pid of nginx can be found at /opt/nginx/logs/nginx.pid. Although this may vary depending on where nginx is installed and how it was configured. Let's now say the pid was 12345 execute the following command…

```
sudo kill -s HUP 12345
```

Where HUP is the hangup signal. You can see the [nginx wiki](http://wiki.nginx.org/CommandLine) for signals that can be sent to nginx.

The wiki states the HUP signal 1. Reloads config; 2. Start the new worker processes with a new configuration; 3. Gracefully shutdown the old worker processes.
