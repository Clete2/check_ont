# check_ont Nagios Plugin
check_ont is a [Nagios Plugin](https://nagios-plugins.org/), compatible with a wide variety of network monitoring software.

check_ont will read the 8311 firmware's metrics page, and create metrics for each emitted variable. I have defined sensible defaults for the metrics based on [ont.wiki](https://ont.wiki)'s documentation.

# Installation
The script uses Bash and Python (to avoid jq requirement), which were both available on my [LibreNMS](https://librenms.org) installation.

I run LibreNMS in Docker, so I copied this into the `monitoring-plugins` folder available to me, and then restarted the stack, and I was able to see `check_ont` on the Services page.

Next, I added the `check_ont` check to my X-ONU-SFPP host, and now I have metrics.

# Example metrics

![metrics](./docs/metrics.png)

# Disclaimer

This README was totally human-written, and the script was totally vibe coded.
