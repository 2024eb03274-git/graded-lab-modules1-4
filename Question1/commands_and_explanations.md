### Step 1: User Identity Verification

**Command:**
```bash
whoami
groups
id
```
**Output:**  
(See outputs.txt)

**Explanation:**  
I verified that I am logged in as the user `coder` using `whoami`. The `groups` and `id` commands confirmed that my account belongs to the `coder` and `sudo` groups, proving my user identity and privileges.

### Step 2: Workspace Validation

**Command:**
```bash
pwd
ls -l
```
**Output:**
(See outputs.txt)

**Explanation:**
I displayed my current working directory using `pwd` and listed all files in that location with detailed information using `ls -l`, which shows permissions, ownership, file size, and modification dates.

### Step 3: Environment Confirmation File

**Command:**
```bash
echo "Linux user environment verified" > user_info.txt
cat user_info.txt
```
**Output:**
(See outputs.txt)

**Explanation:**
I created the file `user_info.txt` and wrote the required verification message into it using output redirection. The `cat` command confirmed that the content was written successfully.

### Step 4: File Integrity Check

**Command:**
```bash
wc -m user_info.txt
```
**Output:**
(See outputs.txt)

**Explanation:**
I used `wc -m` to count the number of characters in the file `user_info.txt`. This confirms the file’s integrity by showing the exact character count including the newline.

### Step 5: Learning the mkdir Command

**Command:**
```bash
mkdir --help
```
**Output:**
(See screenshot in screenshots folder)

**Explanation:**
Since manual and info pages are not available on this system, I used `mkdir --help` to review the command documentation. I learned that the `-p` option allows creating parent directories automatically and prevents errors if the directory already exists.

### Step 6: Home Directory Inspection

**Command:**
```bash
ls -1 ~ | sort
```
**Output:**
(See outputs.txt)

**Explanation:**
I listed all files and directories in my home directory and sorted them alphabetically using ls -1 ~ | sort. This provides an ordered view of all items located in my home folder.

