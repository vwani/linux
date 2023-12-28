# Change passwords and adjust password aging for local user accounts

## Change password 
> \# passwd username

## Adjust password aging 
View current password aging settings
> \# chage -l username

Change current password aging settings
> \# chage --mindays 7 --maxdays 90 --warndays 5 username


Option|Description
:---:|---
-m or --mindays|Specifies minimum number of days password must be active before it can be changed by user
-M or --maxdays|Specifies maximum number of days a password can be active before expiring
-W or --warndays|Specifies number of days a warning is issued to the user before an impending password expiry
