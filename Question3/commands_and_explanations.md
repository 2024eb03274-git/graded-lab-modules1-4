 Question 3 – File Links and Disk Usage

### Step 1: File Creation

**Command:**
```bash
echo "Sample file for link testing" > sample_data.txt
cat sample_data.txt
```
**Output:**
(See outputs.txt)

**Explanation:**
I created a file named `sample_data.txt` and added sample text to it. The `cat` command verified that the file content was written correctly.

### Step 2: Hard Link Creation

**Command:**
```bash
ln sample_data.txt sample_hard.txt
ls -l sample_data.txt sample_hard.txt
```
**Output:**
(See outputs.txt)

**Explanation:**
I created a hard link named `sample_hard.txt` pointing to the same inode as `sample_data.txt`. The link count of 2 in the output confirms that both files reference the same data on disk.

### Step 3: Symbolic Link Creation

**Command:**
```bash
ln -s sample_data.txt sample_soft.txt
ls -l sample_soft.txt
```
**Output:**
(See outputs.txt)

**Explanation:**
I created a symbolic link named `sample_soft.txt` that points to `sample_data.txt`. The arrow in the output confirms that this file is a soft link reference to the original file.

### Step 4: Inode Verification

**Command:**
```bash
ls -li sample_data.txt sample_hard.txt sample_soft.txt
```
**Output:**
(See outputs.txt)

**Explanation:**
I listed the inode numbers for the original file, hard link, and symbolic link using `ls -li`. This output allows me to compare which files reference the same inode on disk.

### Step 5: Inode Analysis

**Command:**  
(No command required – analysis only)

**Output:**  
(See outputs.txt)

**Explanation:**  
The files `sample_data.txt` and `sample_hard.txt` share the same inode number, which means they point to the same physical data on disk. The symbolic link `sample_soft.txt` has a different inode because it only stores a reference path to the original file.

### Step 6: File Metadata Inspection

**Command:**
```bash
stat sample_data.txt
```
Explanation:
This command displays detailed metadata about the file including size, permissions, inode number, owner, and timestamps. It helps understand how Linux tracks file properties internally.

### Step 7: Disk Usage Check

**Command:**
```bash
du -sh ~
```
**Explanation:**
I displayed the total disk space used by my home directory in a human-readable format, which helps me understand how much storage my files are consuming.

### Step 8: File Size Overview

**Command:**
```bash
ls -lh ~
```
**Explanation:**
I listed all files in my home directory using human-readable format to easily view the size of each file and directory.

### Step 9: Link Deletion Test

**Command:**
```bash
rm sample_soft.txt
ls -l sample_data.txt
```
**Explanation:**
I deleted the symbolic link and then listed the original file to verify that it still exists, proving that removing a soft link does not affect the original file.

## Step 10 — Disk Utility Demonstration (du and df)

### Command 10.1
```bash
du -sh ~
```
**Explanation:**
This command shows the total disk space used by my home directory (~) in a summarized, human-readable format.

### Command 10.2
```bash
du -ah ~ | head
```
**Explanation:**
This command lists disk usage for individual files and directories inside my home directory in human-readable format, and head limits the output to the first entries.

### Command 10.3
```bash
df -h
```
**Explanation:**
This command displays filesystem disk usage, showing total size, used space, available space, percentage used, and mount points in a human-readable format.
