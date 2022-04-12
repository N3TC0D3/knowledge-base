# Windows
## Show hidden / unused devices in device manager
Finding and uninstalling drivers of devices inside Windows that are no longer attached to your computer can be quite hard. 
Here is a way to make hidden and unused devices visible in the device manager:
1. Open System properties
2. Go to Environment variables.
3. Create an environment variable called `devmgr_show_nonpresent_devices` and set the value to `1`