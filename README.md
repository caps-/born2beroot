# born2beroot

- https://github.com/IsCoffeeTho/42-Born2BeRoot
- https://baigal.medium.com/born2beroot-e6e26dfb50ac

# where I'm up to

- lighttpd is installed, get going with the rest..
- https://websiteforstudents.com/install-wordpress-on-ubuntu-16-04-lts-with-lighttpd-mariadb-and-php-7-1-support/
- https://www.how2shout.com/linux/how-to-install-lighttpd-web-server-on-debian-11-bullseye-or-ubuntu-20-04/

# sofie's laptop

- Done the main bit, no bonuses yet.

# shit to remember
## change the hostname

- Check the current hostname
```
$ hostnamectl
```
- Change the hostname
```
$ hostnamectl set-hostname <whateverNameYouWantGoesHere>
```
- Change /etc/hosts file
```
$ sudo vim /etc/hosts
```
- Change the old hostname to the new new one
```
127.0.0.1       localhost
127.0.0.1       <whateverNewNameYouWantGoesHere>
```
- Reboot and check the change
```
$ sudo reboot
$ hostnamectl
```
