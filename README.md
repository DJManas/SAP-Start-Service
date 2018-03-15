# SAP Start Service

This simple script should start SAP using ```sudo service start sap``` command.

Just upload it to ```/etc/init.d/``` directory and assign correct authorizations.

Just written, because SAP server was restarting because of HW error and I needed autostart so users can continue working on boot and I don't have to start it manually.

This time it works on Oracle Linux, for other ones this might need a little tampering.

# TO-DO
- Notification on error, now it starts and when error occurs, nothing happens
- Make it systemd friendly (maybe it is, haven't looked for it yet)
- Implement SAP HANA enhancements - if needed
- Make it friendly for other supported Linux distributions, now only Oracle Linux (RHEL) fiendly
- Make use of configuration file, now variables should be changed inside service file (something like on FreeBSD's /etc/make.conf or Debian's /etc/defaults/*)
- Additional checks according to ports binded, not only /var/lock/sap.lock
- Check for return commands of previous commands or parse log files
- Check if user, under which it should be run, exists
