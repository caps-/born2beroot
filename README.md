# born2beroot

- https://github.com/IsCoffeeTho/42-Born2BeRoot
- https://baigal.medium.com/born2beroot-e6e26dfb50ac
- https://github.com/hanshazairi/42-born2beroot
- https://github.com/ayoub0x1/born2beroot

# where I'm up to

- lighttpd is installed, get going with the rest..
- https://websiteforstudents.com/install-wordpress-on-ubuntu-16-04-lts-with-lighttpd-mariadb-and-php-7-1-support/
- https://www.how2shout.com/linux/how-to-install-lighttpd-web-server-on-debian-11-bullseye-or-ubuntu-20-04/

# sofie's laptop

- Bonuses, just installed lighttpd

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
- Deleting ufw rules
```
$ sudo ufw status numbered
$ sudo ufw delete (that number, for example 5 or 6)
```
- Adding a new user
```
$ sudo adduser <newusername>
```
- Add usergroup
```
$ sudo groupadd <newgroupname>
```
- Check groups
```
$ getent grouup
```
- Add user to groupp
```
$ sudo usermod -aG <groupname> <username>
```
- Check if user is in group
```
$ getent group <groupname>
```
- Check which groups current acct belongs to
```
$ groups
```
- Stop and start cron
```
$ sudo /sbin/service cron stop
$ sudo /sbin/service cron start
```
