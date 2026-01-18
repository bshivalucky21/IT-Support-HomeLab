
# Ticket 001 - Access denied to S: drive

## User Report
User cannot access S: drive. Error: Access denied.

## Triage Questions Asked
- Which folder/share?
- When did it start?
- Any recent password change?
- Are other users affected?

## Investigation
- Confirmed user group membership in AD
- Checked Share permissions and NTFS permissions
- Access-Based Enumeration enabled (expected behavior)

## Fix
- Added user to correct security group / updated NTFS permissions

## Outcome
User confirmed access restored.

## Notes
Recommend managing access via AD groups + NTFS rather than direct user permissions.
