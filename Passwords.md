# Change passwords and adjust password aging for local user accounts

## Password Actions
Change password for a user account
> \# passwd username

View password status for a user account
> \# passwd -S username

output fields: 
username|status|date last changed|min age|max age|warn period|inactive period
---|---|---|---|---|---|---|

status|description
:---:|---
P|Usable Password
NP|No Password
L|Locked Password

View password status for all accounts
> \# passwd -Sa

Delete password from an account (able to log in without password)
> \# passwd -d username

Lock a user account
> \# passwd -l username

Unlock user account
> \# passwd -u username

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
