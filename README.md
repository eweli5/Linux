# Daily Linux Commands

A compact, copy-paste-ready reference for Linux tasks.

---
## Common Commands in my Homelab

```bash
systemctl start smbd    # start the smb share in the network
systemctl stop smbd     # stop the smb share in the network
lsblk                   # list drives
mount                   # mount drive
umount                  # unmount drive

# Download latest binary
wget https://github.com/cloudflare/cloudflared/releases/latest/download/cloudflared-linux-amd64

# Make executable
chmod +x cloudflared-linux-amd64

# Move to PATH
sudo mv cloudflared-linux-amd64 /usr/local/bin/cloudflared

cloudflared tunnel login
cloudflared tunnel create my-tunnel
cloudflared tunnel run jellyfin-tunnel  # start a cloudflared tunnel for example: jellyfin

```
## Make Python Programs & Execute them

```bash
sudo nano /usr/local/bin/filename  # create python program
"#!usr/bin/env python3"   # make this the first line of your code
sudo chmod +x /usr/local/bin/filename # make program executable
```
---

## Navigation

```bash
pwd                    # show current directory
ls -lah                # list files (detailed, human-readable)
cd /path/to/dir        # change directory
cd ..                  # go up one directory
cd ~                   # go to home directory
tree                   # show folder structure (if installed)
```

---

## File & Directory Management

```bash
touch file.txt         # create empty file
mkdir folder           # create directory
mkdir -p a/b/c         # create nested directories
cp file.txt copy.txt   # copy file
cp -r dir1 dir2        # copy directory
mv file.txt new.txt    # rename/move file
rm file.txt            # delete file
rm -rf folder          # delete directory recursively
```

---

## Viewing & Editing Files

```bash
cat file.txt           # print file contents
less file.txt          # scroll through file
head -n 20 file.txt    # first 20 lines
tail -n 20 file.txt    # last 20 lines
tail -f logfile.log    # follow live logs
nano file.txt          # simple editor
vim file.txt           # advanced editor
```

---

## Search & Find

```bash
find . -name "file.txt"     # find file
grep "text" file.txt        # search text in file
grep -r "text" .            # recursive search
which python                # locate binary
```

---

## Permissions & Ownership

```bash
chmod +x script.sh     # make executable
chmod 755 file         # set permissions
chown user:group file  # change owner
```

---

## System Monitoring

```bash
top                    # live process view
htop                   # better top (if installed)
ps aux                 # list processes
kill PID               # kill process
df -h                  # disk usage
du -sh folder          # folder size
free -h                # memory usage
uptime                 # system uptime
```

---

## Networking

```bash
ip a                   # show IP addresses
ping google.com        # test connectivity
curl ifconfig.me       # get public IP
wget URL               # download file
netstat -tuln          # open ports
ss -tuln               # modern netstat alternative
```

---

## Package Management (Debian/Ubuntu)

```bash
sudo apt update        # update package list
sudo apt upgrade       # upgrade packages
sudo apt install pkg   # install package
sudo apt remove pkg    # remove package
```

---

## Archives & Compression

```bash
tar -czvf file.tar.gz folder   # compress
tar -xzvf file.tar.gz          # extract
zip -r file.zip folder         # zip
unzip file.zip                 # unzip
```

---

## Disk & File Info

```bash
file filename          # file type
stat filename          # detailed info
lsblk                  # disk layout
mount                  # mounted drives
```

---

## Productivity Shortcuts

```bash
history                # command history
!!                     # repeat last command
!123                   # run command #123
clear                  # clear terminal
alias ll="ls -lah"     # create shortcut
```

---

## SSH & Remote Access

```bash
ssh user@host              # connect to server
scp file user@host:/path   # copy file to server
rsync -avz src/ dest/      # sync directories
```

---

## Git (Basic Workflow)

```bash
git clone URL
git status
git add .
git commit -m "message"
git push
git pull
```

---

## System Services (systemd)

```bash
systemctl status service        # check service status
systemctl start service         # start service
systemctl stop service          # stop service
systemctl restart service       # restart service
systemctl reload service        # reload config without full restart
systemctl enable service        # enable at boot
systemctl disable service       # disable at boot
systemctl list-units --type=service --all   # list services
journalctl -u service           # view logs for a service
journalctl -xe                  # recent system logs (detailed)
```

---

## Package Management (Arch Linux)

```bash
sudo pacman -Syu        # update system
sudo pacman -S pkg      # install package
sudo pacman -R pkg      # remove package
sudo pacman -Ss name    # search package
sudo pacman -Qi pkg     # package info
```

---

## Package Management (Fedora / RHEL)

```bash
sudo dnf check-update   # check updates
sudo dnf upgrade        # upgrade system
sudo dnf install pkg    # install package
sudo dnf remove pkg     # remove package
sudo dnf search name    # search package
sudo dnf info pkg       # package info
```

---

## Optional Improvements

```bash
# safer file operations
alias cp="cp -i"
alias mv="mv -i"
alias rm="rm -i"

# useful tools
sudo apt install htop tree ncdu
```
