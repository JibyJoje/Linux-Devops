# Linux for Devops
This repository contains basics about linux which is essential enough for Devops Engineers to perform their  daily tasks

## Linux Filesystem Hierarchy:

| Directory Name | Description  |
|--|--|
|/|This is top level directory <br/>It is parent Directory for all other directories <br/>It is called as the `Root` Directory <br/>Similar to the `C:/` in Windows <br/>|
|/root |It is the home directory for the `root user` (Super User)</br>it provides working environment for root user</br>Similar to `C:\Documents and Settings\Administrator`|
|/home|This is where the home directory for normal users are present</br>It provides a working environment for other users|
|/usr|By default all softwares are installed in the `/usr` directory</br>It stands for Unix Sharable Resources</br>Similar to `C:\Program Files`|
|/bin|It contains the commands used by all users|
|/sbin|It contains the commands used by only the root user|
|/var|It contains variable data like mails and log files|

## Basic Linux Commands:

|Command|Description|
|--|--|
|date|shows the current date and time|
|cal|show the current month calendar|
|uptime|shows how long the system/server has been running|
|whoami|Shows who are you logged in as|
|finger|Display information about user|
|users/id|Shows user information|
|man|Manual of command|
|username|Shows your username|
|who/w|Shows who is online|

## Read a file:

|Command|Description|
|--|--|
|ls|Directory listing|
|cat|view the entire contents of the file|
|less|view a file page by page|
|more|output contents of the file|
|head|output first 10 lines of a file|
|tail|output last 10 lines of a file|
|page|display file page by page|
|pwd|prints the present working directory|

## Create or Delete a file: 

|Command|Description|
|--|--|
|touch|Creates an empty file|
|cat > filename|Create file and allow to write|
|nano|Create the filename if the file doesn't exist|
|vi|create and edit file if the file doesn't exist|
|rm|remove a file|
|mkdir|Create a Directory|
|rmdir|remove an empty Directory|
|rm -rf|Remove a directory if it has contents|
|cd|change the current directory|

## Edit or Append a file:

|Command|Description|
|--|--|
|vi or nano|You can edit already existing files using vi, vim or nano|
|cat > filenam|This will add new contents to empty file and override contents of existing file|
|cat >> filename|This will append any new contents to the existing file|

## Manage files or directories:

|Command|Description|
|--|--|
|cp|copy a file from source to destination|
|mv|move a file from source to destination|
|mv|move command can also be used to rename a file|
|find|find files or directories, similar to search in windows.<br/> `-name` can be used to search based on file name <br/> `-user` canb be used to search files belong to the user <br/> `-group` can be used to search files belonging to groups |
|diff|gives the difference between two files|
|file|Determine the type of file|
|grep|search for a particular pattern in a file or output|
|sed|search a word and replace it. Similar to Find and replace in windows|

## User Management:

|Command|Description|
|--|--|
|Super or Root User|Admin User with all privileges|
|System User|Users created by softwares or applications|
|Normal User|Users created by root user|
|useradd `<flag> <username>`|Create a user in Linux System<br/>`-u` - user ID <br/>`-G` - Secondary Group<br/>`-g` - Primary Group<br/>`-d` - home directory<br/>`-c` - Comment<br/>`-s` - Default Shell|
|usermod `<flag> <group> <user>|Modify existing user attributes|

## File Permissions

|Command|Description|
|--|--|
|Permission are applied at 3 levels|Owners, Groups and Others|
|Permission are applied in 3 ways|`r` - read<br/>`w` - Write<br/>`x` -Execute|
|chmod|change the permissions of a file or directory<br/>- Symbolic Method<br/>- Absolute Method|
|chown|Change the ownership of the file and this command can only be executed by the root user

- When you execute the `ls -l` command you will see the detailed permissions that are set on the file : 
`-rw-r--r--  1 j0j07as staff 3505 Jul  6 10:04 Linux-Devops.md`
    - Let us consider the example of `-rw-r--r--` in this case
    - The first `-` indicates the type of file, in this case its a normal file. It would have been `d` if this was a directory
    - The next 3 `rw-` indicate the owner permissions, which means that the owner of the file `j0j07as` has read and write permissions on this file.
    - The next 3 `r--` indicate the group permission, which mean any user who is part of the group that is owned by the file `staff` will have read permission
    - And the last 3 `r--` indicate that any user who is not a user or not a part of the group will have only read permission.

## System Management:

|Command|Description|
|--|--|
|history|list of all commands that were executed by the user|
|free|free memory of the server|
|cat /proc/meminfo|Display Memory Information|
|cat /proc/cpuinfo|Display CPU Information|
|uname -a|Show kernel Information|
|du|Display Disk Usage|
|yum|install red-hat packages|

## Networking:

|Command|Description|
|--|--|
|hostname|Displays the hostname of the server|
|ping {ip}|checks the connectivity of a destination server over the N/W|
|wget|Download packages/softwares into the host|
|ifconfig|Displays the IP address of the server|
|telnet|connect to remote host/check port availability|
|curl|Access the appliation as from a browser|
|telnet|Check the availability of the port on a system|

## Services:

|Command|Description|
|--|--|
|service|This command is used to control the services<br/>
`service {service-name} status` --> Check the status of the service<br/>
`service {service-name} start` --> Start the service<br/>
`service {service-name} stop` --> Stop the service<br/>
`service {service-name} reload` --> Reload the service<br/>
`service {service-name} restart` --> Restart the service|
|chkconfig|Control if the service should be on/off on boot time<br/>
`chkconfig --list` --> List all available service<br/>
`chkconfig {service-name} on` --> Keep the service running even after restart<br/>
`chkconfig {service-name} off` --> Make the service unavailable after restart|