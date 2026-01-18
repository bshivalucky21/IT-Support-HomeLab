# IT-Support-HomeLab>

# IT Support Home Lab (Active Directory + File Server + osTicket)

This lab demonstrates hands-on IT Support / Service Desk skills in a small enterprise-style environment:
- Windows Server 2022 Domain Controller (AD DS + DNS)
- Windows 11 domain-joined client
- File Server shares with NTFS + Share permissions and Access-Based Enumeration (ABE)
- Group Policy (GPO) controls (lockout, restrictions, drive mapping)
- osTicket on Ubuntu (ticket intake + agent workflow)

## Lab Environment
- DC01: Windows Server 2022 (AD DS, DNS, File Services)
- W11-CLIENT: Windows 11 (domain joined)
- Ubuntu: osTicket (web-based ticketing system)

## Key Scenarios (Runbooks)
- [User locked out](runbooks/user-locked-out.md)
- [Cannot access S: drive (Access denied)](runbooks/cannot-access-s-drive.md)
- [DNS not resolving](runbooks/dns-not-resolving.md)
- [Restricted Control Panel (GPO)](runbooks/restricted-control-panel.md)

## Ticket Examples
- [Ticket 001 - Access denied to S: drive](ticket-examples/ticket-001-access-denied.md)
- [Ticket 002 - User locked out](ticket-examples/ticket-002-account-lockout.md)

## Evidence
See: [Screenshots](screenshots/)
