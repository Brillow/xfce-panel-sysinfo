# xfce-panel-sysinfo
Simple scripts to display system information in XFCE panels (or anywhere else)

# Usage
In XFCE panels you can add a "General Monitor" item to the panel and have it call one of these scripts every ... seconds. The information will then be displayed in the panel.

Be careful when adding the cpu script. The refresh-period should be longer than 1s since mpstat averages the load over a period of one second. Shorter refreshes might lead to errors.

# Scripts
## ...fs
Monitor remaining free space on the given device. Change the device inside the script to whatever device you want to monitor.

Only needs df, tail and awk which should be preinstalled on most systems.

## cpu
Uses mpstat to determine current cpu-load-percentage.

Packages needed: sysstat

## mem
Uses the free command to determine current memory usage.

## swap
Uses the free command to determine current swap usage.

## uptime
Uses the uptime command and awk to print current uptime.

## wifi
Gets information about wifi reception from /proc/net/wireless
