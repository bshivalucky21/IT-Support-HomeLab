# Runbook: Control Panel restricted by GPO

## Symptoms
- User receives: "This operation has been cancelled due to restrictions..."
- Control Panel/Settings blocked

## Cause
- Group Policy applied to user or computer OU

## Troubleshooting
1. Run on client: `gpresult /r` (confirm applied GPOs)
2. In GPMC: verify the GPO is linked to correct OU
3. Verify Security Filtering / WMI filters

## Resolution
- If user should have access: remove from OU or adjust GPO scope
- Run: `gpupdate /force` on client

## Validation
- Control Panel access behaves as expected
