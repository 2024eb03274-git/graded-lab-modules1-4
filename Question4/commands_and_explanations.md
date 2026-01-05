# Question 4 — System Monitoring & Processes

## Step 1 — System Uptime Verification

### Command
```bash
uptime
```
**Explanation:**
This command displays how long the system has been running since the last reboot, the number of active users, and the system load averages for the last 1, 5, and 15 minutes.

## Step 2 — User Process Listing

### Command
```bash
ps -u $USER
```
**Explanation:**
This command lists all processes currently running under my user account, including their PID, terminal, CPU time, and the command name.

## Step 3 — CPU Usage Analysis

### Command
```bash
top -u $USER
```
**Explanation:**
This command displays real-time information about all processes owned by my user account and allows identifying which process is consuming the most CPU resources.

## Step 4 — Background Process Execution

### Command
```bash
sleep 300 &
jobs
```
Explanation:
This command starts the `sleep` process in the background, and the `jobs` command confirms that the background process is currently running.

## Step 5 — Process Priority Management

### Command
```bash
ps -o pid,ni,cmd -u $USER | grep sleep
renice 10 -p 453
ps -o pid,ni,cmd -u $USER | grep sleep
```
**Explanation:**
This command changes the niceness value of the running Python process with PID 276 from 0 to 10, lowering its priority, and the output confirms that the new priority has been applied.

## Step 6 — Memory Usage Monitoring

### Command
```bash
free -h
```
**Explanation:**
This command displays memory usage in a human-readable format, including total, used, free, shared, buff/cache, and available memory.

## Step 7 — Disk Space Inspection

### Command
```bash
df -h ~
```
**Explanation:**
This command displays the disk space usage of the filesystem where my home directory is stored, showing total size, used space, available space, and usage percentage.

## Step 8 — Shell Identification

### Command
```bash
echo $SHELL
```
**Explanation:**
This command displays the path and name of the shell currently being used, which in this case is the Bash shell.

## Step 9 — Output Redirection

### Command
```bash
uname -a > system_report.txt
cat system_report.txt
```
**Explanation:**
This command redirects the output of the `uname -a` system information command into the file `system_report.txt`, and the second command confirms the contents of the file.

