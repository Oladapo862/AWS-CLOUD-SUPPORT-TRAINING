# Day 5 – Troubleshooting

## Issue – Unable to Copy a File to Another Directory

### Problem

While attempting to copy a file from one directory to another, the command failed because I specified the wrong destination path.

### Cause

I used:

```bash
mv files newfolder/
```

I assumed the destination directory was in my current location. However, the target directory was located one level above the current directory. Because of this, Linux could not find the destination path.

### Resolution

I corrected the destination path by using the parent directory reference:

```bash
mv files ../newfolder/
```

Using `..` moved up one directory level before accessing the destination folder, allowing the command to complete successfully.

### Lesson Learned

* Always confirm your current location with `pwd` before moving or copying files.
* Use relative paths correctly:

  * `.` refers to the current directory.
  * `..` refers to the parent directory.
* Understanding the Linux directory structure helps avoid path-related errors when managing files.

---

# Conclusion

This troubleshooting exercise improved my understanding of relative paths in Linux. After identifying that the destination directory was not in my current location, I corrected the command by referencing the parent directory, and the file operation completed successfully.
