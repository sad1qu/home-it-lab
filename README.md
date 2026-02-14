## Scenario 1: User cannot access a file

**Problem:**  
User reported lack of access to a file.

**Investigation:**  
Verified file existence and checked permissions. Initially, the file was readable by all users.
Access was then restricted to reproduce the issue.

**Resolution:**  
Created a dedicated group, assigned the file to that group, and added the user to it.
After refreshing the user session, access was restored following the principle of least privilege.

**Outcome:**  
User successfully accessed the file without granting excessive permissions.

## Scenario 2: File cannot be deleted

**Problem:**  
User was able to read a file but could not delete it.

**Investigation:**  
Checked file permissions and confirmed that deletion was blocked due to missing write permissions on the parent directory.

**Resolution:**  
Assigned the directory to a dedicated group and granted write permissions to that group only.

**Outcome:**  
User successfully deleted the file while maintaining proper access control.

## Scenario 3: High CPU usage

**Problem:**  
System performance was reported as slow.

**Investigation:**  
Used the `top` command to analyze CPU and memory usage.  
Identified a process consuming nearly 100% CPU.

**Resolution:**  
Terminated the process using `kill` after confirming it was not critical.

**Outcome:**  
CPU usage returned to normal levels and system performance stabilized.
