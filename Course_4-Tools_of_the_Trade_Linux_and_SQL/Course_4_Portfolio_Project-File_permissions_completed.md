# 🛡️ File Permissions in Linux

## 📘 Project Description

In this scenario, I worked as a security professional responsible for managing file system permissions on a Linux machine used by a research team. My task involved checking current file and directory permissions, interpreting those permissions, and modifying them to ensure only authorized users had the correct access. This included managing hidden files, removing unauthorized access for “others,” and securing a sensitive directory.

---

## 🔍 Check File and Directory Details

To check file and directory permissions, I used the following command:

```bash
ls -la /home/researcher2/projects
```

The output showed the following file permissions:

project_k.txt: -rw-rw-rw-
project_m.txt: -rw-r-----
project_r.txt: -rw-rw-r--
project_t.txt: -rw-rw-r--
project_x.txt: --w--w----
drafts/ directory: drwx--x---

### 🧾 Describe the Permission String

Example: -rw-rw-r-- (for project_t.txt)

This 10-character string shows the type of file and its permissions:

- - regular file
- rw- — User has read and write permissions
- rw- — Group has read and write permissions
- r-- — Others have read-only access

So, project_t.txt is readable and writable by the user and group, and readable by others.

### ✏️ Change File Permissions

File: project_k.txt
Issue: File had world-writable access (-rw-rw-rw-), which is not secure.

Command used:

```bash
chmod o-w /home/researcher2/projects/project_k.txt
```

- New permissions: -rw-rw-r--
- Write access was removed from others, ensuring only the user and group can modify the file.

### 👁️ Change File Permissions on a Hidden File

File: .project_x.txt
Issue: Hidden file had write access with no read access — not ideal for sensitive data.

Command used:

```bash
chmod 440 /home/researcher2/projects/.project_x.txt
```

New permissions: -r--r-----
Now only the user and group have read-only access. No access is given to others.

### 📁 Change Directory Permissions

Directory: drafts/
Issue: Directory was executable by others, posing a potential risk.

Command used:

```bash
chmod 700 /home/researcher2/projects/drafts
```

New permissions: drwx------
Only the owner has read, write, and execute permissions. Group and others have no access.

## ✅ Summary

In this task, I:

- Reviewed and updated Linux file permissions using chmod
- Removed unauthorized write access for public files
- Locked down hidden files with read-only restrictions
- Restricted a directory to be accessible only by its owner

These changes help maintain file confidentiality and ensure compliance with organizational security policies on multi-user Linux systems
