# Basic Linux Commands Reference Guide

## Navigation Commands

### `pwd` - Print Working Directory
Shows the current directory you're in.
```bash
pwd
# Output: /home/username
```

### `ls` - List Directory Contents
Lists files and directories in the current location.
```bash
ls                    # Basic listing
ls -l                 # Detailed listing with permissions, size, date
ls -la                # Include hidden files (starting with .)
ls -lh                # Human-readable file sizes
ls /path/to/directory # List specific directory
```

### `cd` - Change Directory
Navigate between directories.
```bash
cd /path/to/directory  # Go to specific directory
cd ..                  # Go up one directory
cd ~                   # Go to home directory
cd -                   # Go to previous directory
cd                     # Go to home directory (same as cd ~)
```

## File and Directory Operations

### `mkdir` - Make Directory
Create new directories.
```bash
mkdir foldername           # Create single directory
mkdir -p path/to/folder    # Create nested directories
mkdir folder1 folder2      # Create multiple directories
```

### `rmdir` - Remove Directory
Remove empty directories.
```bash
rmdir foldername          # Remove empty directory
rmdir -p path/to/folder   # Remove nested empty directories
```

### `rm` - Remove Files and Directories
Delete files and directories.
```bash
rm filename               # Remove file
rm file1 file2           # Remove multiple files
rm -r directory          # Remove directory and its contents recursively
rm -rf directory         # Force remove directory (be careful!)
rm *.txt                 # Remove all .txt files
```

### `cp` - Copy Files and Directories
Copy files or directories.
```bash
cp file1 file2           # Copy file1 to file2
cp file1 /path/to/dest/  # Copy file to destination directory
cp -r dir1 dir2          # Copy directory recursively
cp *.txt backup/         # Copy all .txt files to backup directory
```

### `mv` - Move/Rename Files and Directories
Move or rename files and directories.
```bash
mv oldname newname       # Rename file or directory
mv file1 /path/to/dest/  # Move file to destination
mv *.txt documents/      # Move all .txt files to documents directory
```

## File Content Commands

### `cat` - Display File Content
Display entire file content.
```bash
cat filename             # Display file content
cat file1 file2          # Display multiple files
cat > newfile.txt        # Create new file (Ctrl+D to save)
```

### `less` and `more` - View File Content Page by Page
View large files one screen at a time.
```bash
less filename            # View file with navigation (q to quit)
more filename            # View file page by page (space for next page)
```

### `head` - Display First Lines
Show the beginning of a file.
```bash
head filename            # Show first 10 lines
head -n 20 filename      # Show first 20 lines
head -5 filename         # Show first 5 lines
```

### `tail` - Display Last Lines
Show the end of a file.
```bash
tail filename            # Show last 10 lines
tail -n 20 filename      # Show last 20 lines
tail -f filename         # Follow file changes in real-time
```

### `grep` - Search Text
Search for patterns in files.
```bash
grep "pattern" filename          # Search for pattern in file
grep -i "pattern" filename       # Case-insensitive search
grep -r "pattern" directory/     # Recursive search in directory
grep -n "pattern" filename       # Show line numbers
grep -v "pattern" filename       # Show lines NOT containing pattern
```

## File Permissions and Ownership

### `chmod` - Change File Permissions
Modify file and directory permissions.
```bash
chmod 755 filename       # rwxr-xr-x permissions
chmod +x filename        # Add execute permission
chmod -w filename        # Remove write permission
chmod u+rwx filename     # Add read, write, execute for user
```

Permission numbers:
- 4 = read (r)
- 2 = write (w)  
- 1 = execute (x)
- 7 = read + write + execute (4+2+1)
- 6 = read + write (4+2)
- 5 = read + execute (4+1)

### `chown` - Change File Ownership
Change file owner and group.
```bash
chown user filename           # Change owner
chown user:group filename     # Change owner and group
chown -R user:group directory # Change recursively
```

## System Information Commands

### `ps` - Process Status
Display running processes.
```bash
ps                       # Show processes for current user
ps aux                   # Show all processes with details
ps -ef                   # Show all processes in full format
```

### `top` - Task Manager
Display real-time system processes.
```bash
top                      # Interactive process viewer (q to quit)
htop                     # Enhanced version (if installed)
```

### `df` - Disk Space
Show disk space usage.
```bash
df                       # Show disk space
df -h                    # Human-readable format
df -h /                  # Show space for root partition
```

### `du` - Directory Usage
Show directory space usage.
```bash
du                       # Show disk usage for current directory
du -h                    # Human-readable format
du -sh directory         # Show total size of directory
du -sh *                 # Show size of all items in current directory
```

### `free` - Memory Usage
Display memory usage.
```bash
free                     # Show memory usage
free -h                  # Human-readable format
```

## Network Commands

### `ping` - Test Network Connection
Test connectivity to a host.
```bash
ping google.com          # Ping Google (Ctrl+C to stop)
ping -c 4 google.com     # Ping 4 times only
```

### `wget` - Download Files
Download files from the internet.
```bash
wget http://example.com/file.zip    # Download file
wget -O newname.zip http://...      # Download with new name
```

### `curl` - Transfer Data
Transfer data to/from servers.
```bash
curl http://example.com             # Display webpage content
curl -O http://example.com/file.zip # Download file
```

## Text Processing

### `sort` - Sort Lines
Sort lines in text files.
```bash
sort filename            # Sort alphabetically
sort -n filename         # Sort numerically
sort -r filename         # Reverse sort
```

### `wc` - Word Count
Count lines, words, and characters.
```bash
wc filename              # Show lines, words, characters
wc -l filename           # Count lines only
wc -w filename           # Count words only
```

### `cut` - Extract Columns
Extract specific columns from text.
```bash
cut -d',' -f1 file.csv   # Extract first column from CSV
cut -c1-10 filename      # Extract characters 1-10
```

## Archive and Compression

### `tar` - Archive Files
Create and extract archives.
```bash
tar -cvf archive.tar files/     # Create tar archive
tar -xvf archive.tar            # Extract tar archive
tar -czvf archive.tar.gz files/ # Create compressed archive
tar -xzvf archive.tar.gz        # Extract compressed archive
```

### `zip` and `unzip` - ZIP Archives
Work with ZIP files.
```bash
zip archive.zip file1 file2     # Create ZIP archive
zip -r archive.zip directory/   # Create ZIP of directory
unzip archive.zip               # Extract ZIP archive
```

## Help Commands

### `man` - Manual Pages
Display manual pages for commands.
```bash
man ls                   # Show manual for ls command
man -k search_term       # Search manual pages
```

### `--help` - Command Help
Get help for specific commands.
```bash
ls --help               # Show help for ls command
cp --help               # Show help for cp command
```

### `which` - Find Command Location
Find where a command is located.
```bash
which python            # Show path to python command
which ls                # Show path to ls command
```

## Useful Keyboard Shortcuts

- **Ctrl + C**: Cancel current command
- **Ctrl + D**: Exit/logout
- **Ctrl + L**: Clear screen (same as `clear` command)
- **Ctrl + A**: Move cursor to beginning of line
- **Ctrl + E**: Move cursor to end of line
- **Tab**: Auto-complete commands and filenames
- **Up Arrow**: Previous command in history
- **Ctrl + R**: Search command history

## Tips for Beginners

1. **Start with basic navigation**: Master `pwd`, `ls`, and `cd` first
2. **Use tab completion**: Press Tab to auto-complete commands and file names
3. **Read error messages**: They usually tell you what went wrong
4. **Practice in a safe directory**: Create a test folder to experiment in
5. **Use `man` pages**: When in doubt, check the manual with `man command`
6. **Be careful with `rm -rf`**: This permanently deletes files and directories
7. **Use relative vs absolute paths**: Learn the difference between `./file` and `/home/user/file`

## Common File Path Shortcuts

- `.` = Current directory
- `..` = Parent directory  
- `~` = Home directory
- `/` = Root directory
- `-` = Previous directory (with cd command)

Remember: Linux is case-sensitive, so `File.txt` and `file.txt` are different files!
# Linux Commands for Cloud & DevOps

## Table of Contents
1. [Basic File Operations](#basic-file-operations)
2. [Directory Navigation](#directory-navigation)
3. [File Permissions](#file-permissions)
4. [Text Processing](#text-processing)
5. [System Information](#system-information)
6. [Process Management](#process-management)
7. [Network Commands](#network-commands)
8. [Archive & Compression](#archive--compression)
9. [Package Management](#package-management)
10. [Cloud & DevOps Commands](#cloud--devops-commands)
11. [Docker Commands](#docker-commands)
12. [Kubernetes Commands](#kubernetes-commands)
13. [Git Commands](#git-commands)
14. [System Monitoring](#system-monitoring)
15. [Log Analysis](#log-analysis)

## Basic File Operations

### Creating and Viewing Files
```bash
# Create empty file
touch filename.txt

# Create file with content
echo "Hello World" > file.txt

# Append to file
echo "New line" >> file.txt

# View file content
cat file.txt
less file.txt
head -n 10 file.txt    # First 10 lines
tail -n 10 file.txt    # Last 10 lines
tail -f file.txt       # Follow file changes (useful for logs)
```

### File Operations
```bash
# Copy files
cp source.txt destination.txt
cp -r directory/ new_directory/    # Recursive copy

# Move/rename files
mv oldname.txt newname.txt
mv file.txt /path/to/directory/

# Remove files
rm file.txt
rm -rf directory/    # Remove directory recursively (be careful!)

# Find files
find /path -name "*.txt"
find . -type f -name "config*"
```

## Directory Navigation

```bash
# Current directory
pwd

# Change directory
cd /path/to/directory
cd ~        # Home directory
cd ..       # Parent directory
cd -        # Previous directory

# List directory contents
ls
ls -la      # Long format with hidden files
ls -lh      # Human readable file sizes
ls -lt      # Sort by modification time

# Create directories
mkdir new_directory
mkdir -p path/to/nested/directory
```

## File Permissions

```bash
# View permissions
ls -l file.txt

# Change permissions
chmod 755 file.txt           # rwxr-xr-x
chmod +x script.sh           # Add execute permission
chmod -w file.txt            # Remove write permission

# Change ownership
chown user:group file.txt
chown -R user:group directory/

# Change group
chgrp groupname file.txt
```

## Text Processing

```bash
# Search in files
grep "pattern" file.txt
grep -r "pattern" directory/     # Recursive search
grep -i "pattern" file.txt       # Case insensitive
grep -v "pattern" file.txt       # Invert match

# Sort and unique
sort file.txt
sort -n numbers.txt             # Numeric sort
uniq file.txt                   # Remove duplicates
sort file.txt | uniq -c         # Count occurrences

# Text manipulation
sed 's/old/new/g' file.txt      # Replace text
awk '{print $1}' file.txt       # Print first column
cut -d',' -f1 file.csv          # Cut first field (CSV)
```

## System Information

```bash
# System info
uname -a                # Kernel info
hostname                # System hostname
whoami                  # Current user
id                      # User and group IDs

# Hardware info
lscpu                   # CPU information
free -h                 # Memory usage
df -h                   # Disk usage
lsblk                   # Block devices
lsusb                   # USB devices
lspci                   # PCI devices

# System status
uptime                  # System uptime
date                    # Current date/time
cal                     # Calendar
```

## Process Management

```bash
# View processes
ps aux                  # All processes
ps -ef                  # Full format
pgrep process_name      # Find process ID

# Process monitoring
top                     # Real-time process viewer
htop                    # Enhanced top (if installed)
jobs                    # Active jobs

# Process control
nohup command &         # Run command in background
kill PID                # Kill process by ID
killall process_name    # Kill by name
pkill pattern          # Kill by pattern

# Background processes
command &              # Run in background
fg                     # Bring to foreground
bg                     # Send to background
disown                 # Detach from shell
```

## Network Commands

```bash
# Network info
ip addr                 # IP addresses
ip route               # Routing table
netstat -tuln          # Network connections
ss -tuln               # Socket statistics

# Network testing
ping google.com
traceroute google.com
nslookup domain.com
dig domain.com

# Download files
wget https://example.com/file.zip
curl -O https://example.com/file.zip
curl -X POST -H "Content-Type: application/json" -d '{"key":"value"}' https://api.example.com
```

## Archive & Compression

```bash
# Tar operations
tar -cvf archive.tar files/        # Create tar archive
tar -czvf archive.tar.gz files/    # Create compressed archive
tar -xvf archive.tar               # Extract tar archive
tar -xzvf archive.tar.gz           # Extract compressed archive
tar -tvf archive.tar               # List archive contents

# Other compression
zip -r archive.zip directory/
unzip archive.zip
gzip file.txt
gunzip file.txt.gz
```

## Package Management

### Ubuntu/Debian (apt)
```bash
# Update package list
sudo apt update

# Upgrade packages
sudo apt upgrade

# Install package
sudo apt install package_name

# Remove package
sudo apt remove package_name
sudo apt purge package_name     # Remove with config files

# Search packages
apt search keyword
apt list --installed
```

### CentOS/RHEL (yum/dnf)
```bash
# Update packages
sudo yum update
sudo dnf update     # For newer versions

# Install package
sudo yum install package_name
sudo dnf install package_name

# Remove package
sudo yum remove package_name

# Search packages
yum search keyword
yum list installed
```

## Cloud & DevOps Commands

### System Services (systemd)
```bash
# Service management
sudo systemctl start service_name
sudo systemctl stop service_name
sudo systemctl restart service_name
sudo systemctl reload service_name

# Service status
systemctl status service_name
systemctl is-active service_name
systemctl is-enabled service_name

# Enable/disable services
sudo systemctl enable service_name
sudo systemctl disable service_name

# View logs
journalctl -u service_name
journalctl -f                   # Follow logs
journalctl --since "1 hour ago"
```

### Cron Jobs
```bash
# Edit crontab
crontab -e

# List cron jobs
crontab -l

# Remove all cron jobs
crontab -r

# Example cron job (runs every day at 2 AM)
# 0 2 * * * /path/to/script.sh
```

### Environment Variables
```bash
# View environment variables
env
printenv
echo $PATH

# Set environment variable
export VAR_NAME=value
export PATH=$PATH:/new/path

# Make permanent (add to ~/.bashrc or ~/.profile)
echo 'export VAR_NAME=value' >> ~/.bashrc
source ~/.bashrc
```

## Docker Commands

```bash
# Container management
docker run -d --name container_name image_name
docker start container_name
docker stop container_name
docker restart container_name
docker rm container_name

# View containers
docker ps                       # Running containers
docker ps -a                    # All containers

# Image management
docker images                   # List images
docker pull image_name          # Download image
docker build -t image_name .    # Build image from Dockerfile
docker rmi image_name           # Remove image

# Container interaction
docker exec -it container_name bash
docker logs container_name
docker logs -f container_name   # Follow logs

# Docker Compose
docker-compose up -d
docker-compose down
docker-compose logs -f
docker-compose ps
```

## Kubernetes Commands

```bash
# Cluster info
kubectl cluster-info
kubectl get nodes

# Pod management
kubectl get pods
kubectl get pods -A             # All namespaces
kubectl describe pod pod_name
kubectl logs pod_name
kubectl exec -it pod_name -- bash

# Deployments
kubectl get deployments
kubectl create deployment name --image=image_name
kubectl scale deployment name --replicas=3
kubectl rollout status deployment/name

# Services
kubectl get services
kubectl expose deployment name --port=80 --target-port=8080

# Configuration
kubectl get configmaps
kubectl get secrets
kubectl apply -f config.yaml
kubectl delete -f config.yaml

# Namespaces
kubectl get namespaces
kubectl create namespace name
kubectl config set-context --current --namespace=name
```

## Git Commands

```bash
# Repository setup
git init
git clone https://github.com/user/repo.git

# Basic operations
git add .
git add file.txt
git commit -m "Commit message"
git push origin main
git pull origin main

# Branch management
git branch                      # List branches
git branch branch_name          # Create branch
git checkout branch_name        # Switch branch
git checkout -b branch_name     # Create and switch
git merge branch_name           # Merge branch
git branch -d branch_name       # Delete branch

# Status and history
git status
git log
git log --oneline
git diff
git show commit_hash

# Remote management
git remote -v
git remote add origin url
git fetch origin
```

## System Monitoring

```bash
# Resource monitoring
iostat                          # I/O statistics
vmstat                          # Virtual memory stats
sar -u 1 10                    # CPU usage every 1 sec for 10 times

# Disk usage
du -sh *                       # Directory sizes
du -sh /path/to/directory
ncdu                           # Interactive disk usage (if installed)

# Network monitoring
iftop                          # Network usage by connection
nethogs                       # Network usage by process
ss -tuln                       # Socket connections

# Process monitoring
watch -n 1 'ps aux | head'     # Watch command output
pstree                         # Process tree
lsof                           # List open files
lsof -i :80                    # Files using port 80
```

## Log Analysis

```bash
# System logs
tail -f /var/log/syslog        # Follow system log
tail -f /var/log/messages      # Follow messages (CentOS/RHEL)
journalctl -xe                 # Systemd logs with explanations

# Web server logs
tail -f /var/log/nginx/access.log
tail -f /var/log/apache2/error.log

# Application logs
tail -f /var/log/application.log

# Log rotation
logrotate -d /etc/logrotate.conf    # Debug mode
logrotate -f /etc/logrotate.conf    # Force rotation

# Search and analyze logs
grep "ERROR" /var/log/application.log
grep "404" /var/log/nginx/access.log | wc -l
awk '{print $1}' /var/log/nginx/access.log | sort | uniq -c | sort -nr
```

## Advanced File Operations for DevOps

```bash
# File synchronization
rsync -avz source/ destination/
rsync -avz --delete local/ remote:/path/

# File watching
inotifywait -m /path/to/watch
watch -n 5 ls -la

# Symbolic links
ln -s /path/to/original /path/to/link
readlink /path/to/link

# File attributes
lsattr file.txt                # List attributes
chattr +i file.txt             # Make file immutable
```

## Text Processing for DevOps

```bash
# JSON processing with jq (if installed)
curl -s api.example.com/data | jq '.results[0].name'
echo '{"name":"value"}' | jq '.name'

# YAML processing with yq (if installed)
yq eval '.metadata.name' config.yaml

# CSV processing
awk -F',' '{print $2}' data.csv
cut -d',' -f1,3 data.csv

# Log parsing
awk '/ERROR/ {print $1, $2, $NF}' application.log
sed -n '/2023-07-19/,/2023-07-20/p' logfile.log
```

## Tips for DevOps

1. **Use aliases for common commands:**
   ```bash
   alias ll='ls -la'
   alias k='kubectl'
   alias d='docker'
   ```

2. **Pipe commands effectively:**
   ```bash
   ps aux | grep nginx | grep -v grep
   docker ps | awk '{print $1}' | tail -n +2 | xargs docker stop
   ```

3. **Use command history:**
   ```bash
   history | grep docker
   !123                        # Run command number 123 from history
   !!                          # Run last command
   ```

4. **Background and screen sessions:**
   ```bash
   screen -S session_name      # Create named screen session
   screen -r session_name      # Reattach to session
   tmux new -s session_name    # Create tmux session
   tmux attach -t session_name # Attach to tmux session
   ```

Remember to always test commands in a safe environment first, especially those involving file deletion or system modifications!
