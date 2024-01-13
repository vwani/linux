# Create, delete, and modify local user accounts

## Creation
Create user
> \# useradd username

Create user and set and create home dir other than default dir
> \# useradd -d /home/otherdir -m username


Options for useradd
Option|Description
:---:|:---
-d home/dirname|Set dir other than the default, i.e /home/username (Only sets the home dir, doesn't create)
-m|Create home dir if it doesn't exist
-M|Do not create home dir
-g groupname|Add given group as user's primary group
-G grplist|List additional supplementary groups separated by comma
-p pswd|Specify password encrypted with crypt
-e date|Date for account to be disabled in YYYY-MM-DD format
-f days|Number of days after the password expires until account disabled (0: disable immediately, 1: do not disable after password expires)
-r| Create system account with UID < 1000, no home dir
-u uid|Specify unique user id > 999 for user 

## Deletion
Delete user
> \# userdel username

Delete user and user directories
> \# userdel -r username

## Modification
Change username
> \# usermod -l newusername oldusername

Change UID
> \# usermod -u UID username

Add existing user to existing group 

(Overrides existing primary)
> \# usermod -g groupname username

(Overrides existing supplementary)
> \# usermod -G groupname1, groupname2, groupnameN username

(Add new groups to user's existing supplementary group list)
> \# usermod -aG groupname1, groupname2, groupnameN username

Change home directory of a user
> \# usermod -d /home/newfolder username

Change default shell of a user
> \# usermod -s /bin/zsh username

Lock user account (user will not be able to log in to the system)
> \# usermod -L username

Unlock user account
> \# usermod -U username

Set an expiry date to user account
> \# usermod -e YYYY-MM-DD username

## Set/Change Password
Set password for own account
> $ passwd

Set password for account other than own
> \# passwd username
