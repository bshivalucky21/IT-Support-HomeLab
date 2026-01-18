# Runbook: DNS not resolving

## Symptoms
- `ping DC01` fails with "could not find host"
- Websites/names do not resolve
- nslookup times out or shows unknown server

## Likely Causes
- Client DNS is not pointing to Domain DNS (DC)
- Network adapter misconfigured
- DNS service down on DC

## Troubleshooting
1. Run: `ipconfig /all`
   - Confirm DNS server = DC IP (example: 192.168.56.10)
2. Test connectivity:
   - `ping <DC-IP>`
3. Test DNS:
   - `nslookup dc01`
4. Flush cache:
   - `ipconfig /flushdns`

## Resolution
- Set DNS server to the Domain Controller IP
- Restart DNS Client service if required
- If DC DNS service stopped: start it

## Validation
- `ping dc01` works
- Domain login works
