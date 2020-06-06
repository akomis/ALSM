# ALSM
### Arch Linux System Maintenance
A simple bash script that mainly follows the [System maintenance](https://wiki.archlinux.org/index.php/System_maintenance) Arch wiki page instructions but automating most of the procedures.
## Procedures
*as described in the Arch wiki*
- Check if any systemd services have entered in a failed state
- Look for errors in the log files located at /var/log, as well as high priority
- Backup data using rsync
- Upgrade system
- Check for orphans and dropped packages
- Update the mirror list
- Clear package cache
- Remove duplicates using rmlint

After successful execution, the script produces report.txt at the script directory where there is a list of any errors by any of the procedures or the script itself. It is highly recommended to check the report and act on any manual user intervention needed.
## Configuration
Before running the script alter any global $variables according to your system/preferences. Each variable has a description of use and a pointer to the script line(s) it is being used.
It is recommended that the script is run through a cron job to keep the system regularly maintained.
## Dependencies
Get all the required packages to run the script at its full potential with  
`sudo pacman -S rsync rmlint`
## Disclaimer
This script is considered safe to use as it follows best practices found in the Arch wiki and it is generally risk averse. However, proper configuration and use of the script is required to get the desired results and by no way is the author of this script responsible for any unwanted results to your system.
