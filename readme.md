
# 2420 Week 11 Lab

# Aline Hammermuller / Andrew Hull

# backup-one - backup files from server-one to the backup-server

## backup-script 

The backup-script is a script that will backup files from server-one to the backup-server using rsync.
The script reads a configuration file that includes the following: 

1. directories to backup
2. an ip address to back them up to (ip address of the backup-server)

## Executable files storage

File backup-script
1. Copy the file backup-script
2. Save it in the directory /opt/backup-script/backup-script
3. Change the permission of the file to turn it executable 
	(type sudo chmod +x backup-script)


## Files backup-service.service and backup-timer.timer

1. Copy the file backup-service.service and backup-timer.timer
2. Save both file in the directory /etc/systemd/system
3. Change the permissions of the files to turn them executable
	(type sudo chmod +x backup-service.service, type sudo chmod +x backup-timer.timer)

4. Type sudo systemctl daemon-reload
5. Type sudo systemctl start backup-service.service
6. Type sudo systemctl enable --now backup-service
7. Type sudo systemctl enable --now backup-timer.timer

## How to backup files: 

1. Create a file called backup.conf typing vim backup.conf.
2. Inform in the first line the IP address of the machine.
3. Inform in the susequent lines the complete path to the files that will be copied.
4. Save the file in the same directory as the backup executable file. 

> The default username used by this script is **user1** so be sure that you have a user with this
> username in your destination host. 
