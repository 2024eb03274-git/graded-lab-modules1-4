### Step 1: Project Workspace Setup

**Command:**
```bash
mkdir ~/documents
ls -ld ~/documents
```
**Output:**
(See outputs.txt)

**Explanation:**
I created a directory named `documents` inside my home directory using `mkdir`. I verified that it was created successfully using `ls -ld`, which shows the directory permissions, owner, and location.

### Step 2: File Creation

**Command:**
```bash
cd ~/documents
touch plan.txt
ls -l plan.txt
```
Output:
(See outputs.txt)

Explanation (1–2 sentences):
I navigated into the `documents` directory and created a new empty file named `plan.txt` using the `touch` command. The `ls -l` command confirmed that the file was created successfully.

### Step 3: Content Addition

**Command:**
```bash
echo "Remember to complete project documentation." > plan.txt
cat plan.txt
```
**Output:**
(See outputs.txt)

**Explanation:**
I added sample text to the file `plan.txt` using output redirection. The `cat` command displayed the contents of the file to confirm that the text was written successfully.

### Step 4: File Metadata Verification

**Command:**
```bash
ls -l plan.txt
```
**Output:**
(See outputs.txt)

**Explanation:**
I displayed the permissions, ownership, size, and timestamp of the file `plan.txt` using `ls -l`. The output confirms that my username appears as the file owner.

### Step 5: File Duplication

**Command:**
```bash
cp plan.txt plan_copy.txt
ls -l plan_copy.txt
```
**Output:**
(See outputs.txt)

**Explanation:**
I created a duplicate of `plan.txt` named `plan_copy.txt` using the `cp` command. The `ls -l` output confirms that the new file was created successfully.

### Step 6: Directory Renaming

**Command:**
```bash
cd ~
mv documents project_documents
ls -ld project_documents
```
**Output:**
(See outputs.txt)

**Explanation:**
I renamed the directory `documents` to `project_documents` using the `mv` command. The `ls -ld` command confirmed that the directory name was changed successfully.

