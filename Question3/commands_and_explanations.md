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


