# Runbook: Cannot access S: drive (Access denied)

## Symptoms
- Drive is mapped but opening it shows: "Access is denied"
- User can access other shares but not this one

## Likely Causes
- Missing NTFS permissions
- Share permissions too restrictive
- User not in correct AD security group
- Access-Based Enumeration hiding folders

## Troubleshooting Steps
1. Confirm path: `\\DC01\Department Shares` 
2. Check user's group membership in AD
3. On file server: verify **Share permissions**
4. Verify **NTFS permissions** (Security tab)
5. Check if Access-Based Enumeration is enabled (may hide folders)

## Resolution
- Add user to correct AD group OR update NTFS permissions to allow required access
- Keep Share permissions broad (e.g., Authenticated Users: Read) and control access via NTFS

## Validation
- User can open S: drive and access required folder(s)
