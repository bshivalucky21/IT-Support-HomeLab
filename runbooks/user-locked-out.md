# User locked out
# Runbook: User locked out

## Symptoms
- User receives: "The referenced account is currently locked out"
- User cannot sign in to domain-joined PC

## Quick Checks
1. Confirm username and device
2. Check if account is locked in AD Users & Computers
3. Verify lockout policy (GPO or FGPP)

## Resolution Steps
1. On DC01: Open **Active Directory Users and Computers**
2. Locate the user account → **Properties**
3. On **Account** tab → tick/untick **Unlock account**
4. If needed: reset password and force change at next login
5. Ask user to retry login

## Root Cause (Typical)
- Multiple failed password attempts (wrong password, cached credentials, mobile/Outlook trying old password)

## Validation
- User can log in successfully
- Event log shows successful logon (optional)

## Notes
- If frequent lockouts occur, check saved credentials on other devices.
