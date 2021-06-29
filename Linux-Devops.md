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
|||