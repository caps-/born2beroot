# born2beroot

- https://github.com/IsCoffeeTho/42-Born2BeRoot
- https://baigal.medium.com/born2beroot-e6e26dfb50ac
- https://github.com/hanshazairi/42-born2beroot
- https://github.com/ayoub0x1/born2beroot

- https://www.codequoi.com/en/born2beroot-03-installing-wordpress-on-a-debian-server/#installing_mariadb_database_manager_for_wordpress

# where I'm up to

OMG don't forget to edit /etc/security/pwquality.conf!!
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
- Check ufw shit
```
$ sudo ufw status 
```
- Deleting ufw rules
```
$ sudo ufw status numbered
$ sudo ufw delete (that number, for example 5 or 6)
```
- Check ssh
```
$sudo systemctl sshd status
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
- Check users password shit
```
$ sudo chage -l <username>
```
- Check partitions
```
$ lsblk
```
- Set up/edit cron job
```
$ sudo crontab -u root -e
```
- Stop and start cron
```
$ sudo /sbin/service cron stop
$ sudo /sbin/service cron start
```
- Check fail2ban shit
```
$ sudo fail2ban-client status
$ sudo fail2ban-client status sshd
$ sudo tail -f /var/log/fail2ban.log
```
# OI, MAKE ALIASES FOR SHIT!
You can't remember shit, so make aliases. For example, in your ~/.bashrc add the following:
```
alias sudo='sudo '
alias cronstart='/sbin/service cron stop'
alias cronstop='/sbin/service cron stop'
```
# `apt` vs `apt-get`

There's layers to this shit, so bear with me. Right, so Debian uses a package manager called `dpkg` which kinda does what it says, it handles packages. APT (Advanced Packaging Tool), which is *not* to be confused with the command `apt`, is a set of package management tools that that are built on top of `dpkg`. Then there are tools built on top of *that* such as `apt-get`. Now tools like `apt-get` are really good, but they're also really complicated in the sense that they almost have too many features and options. This is where `apt` (which is the command for the *Aptitude* tool) comes in. `apt` is build on top of `apt-get`, and esentially simplifies it. A lot of the most widely used features from `apt-get` (and `apt-cache` which sort of like the search tool for `apt-get`) are bundled in or turned on/off as standard with `apt`, with a lot of the more osbscure ones left out.

## Extra Dumb Shit

- Change the prompt a bit, put this in ~/.bashrc, around line 60:
```
PS1='${debian_chroot:+($debian_chroot)}\[\e[0;90m\][\[\e[0;92m\]\u\[\e[0;32m\]@\[\e[0;32m\]\h\[\e[0;90m\]]\[\e[0    ;36m\]\w\[\e[0;90m\]$\[\e[0m\] '
```
