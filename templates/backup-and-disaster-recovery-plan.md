# Backup and Disaster Recovery Plan

**Company:** [COMPANY NAME]
**Version / date:** [VERSION, DATE]
**Owner:** [NAME, TITLE]

## 1. Objectives

- **RPO** (maximum data loss we can accept): [e.g., 24 hours]
- **RTO** (maximum time to restore service): [e.g., 8 hours for email and files, 24 hours for everything else]

## 2. Systems and priority

| System / data | Location | Business impact if lost | Priority | RPO | RTO |
|---|---|---|---|---|---|
| Accounting data | [LOCATION] | [HIGH] | 1 | | |
| Customer records | [LOCATION] | | | | |
| Shared files | [LOCATION] | | | | |
| Email | [Microsoft 365 / Google] | | | | |
| Line-of-business app | [NAME] | | | | |
| Network configuration | firewall, switch, Wi-Fi | | | | |

## 3. Backup standard (3-2-1)

- 3 copies of important data
- 2 different storage types
- 1 copy offsite or offline/immutable (protects against ransomware and fire)

| What | Method | Frequency | Retention | Offsite copy |
|---|---|---|---|---|
| File server | [tool] | nightly | [30 days + 12 months] | [cloud / rotated drive] |
| Cloud email and files | [third-party backup; the provider's recycle bin is not a backup] | daily | [ ] | |
| Servers (image-level) | [tool] | [weekly] | [ ] | |
| Network configs | export | after each change | [ ] | |

Backup credentials are separate from normal admin credentials and are not reachable from the network the backups protect.

## 4. Monitoring

- Backup jobs send success and failure notices to [EMAIL/RMM]
- A person reviews results [daily/weekly] and signs off
- Automated freshness checks alert if the newest backup is older than [26 hours]

## 5. Restore testing

| Test | Frequency | Last tested | Result |
|---|---|---|---|
| Restore a single file | monthly | | |
| Restore a full system to a test machine | quarterly | | |
| Full disaster scenario walk-through | yearly | | |

A backup is not considered valid until a restore has been tested.

## 6. Disaster scenarios and response

| Scenario | First actions | Recovery path |
|---|---|---|
| Ransomware | isolate, follow Incident Response Plan | rebuild clean, restore from offline/immutable backup |
| Server hardware failure | confirm backup is current | restore to spare or virtual host |
| Fire / flood / theft | ensure people are safe first | procure hardware, restore from offsite copy |
| Internet outage | contact ISP, switch to backup connection or mobile hotspot | work from cloud services |
| Accidental deletion | restore from backup or recycle bin | single-file restore |

## 7. Recovery order

1. Network (firewall, internet, DNS/DHCP)
2. Identity (domain controller or cloud directory)
3. File and application servers
4. Business-critical applications
5. User devices

## 8. Contacts and documentation

Keep offline (printed and in a secure place): admin credentials sheet location, vendor support numbers, ISP account details, backup service logins, licence keys, network diagram.

## 9. Review

Review this plan after any major change to systems and at least yearly.
