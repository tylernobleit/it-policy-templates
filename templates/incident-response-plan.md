# Incident Response Plan

**Company:** [COMPANY NAME]
**Version / date:** [VERSION, DATE]
**Plan owner:** [NAME, TITLE]
**Review cycle:** at least yearly, and after every significant incident

## 1. Purpose and scope

How [COMPANY NAME] detects, responds to and recovers from security incidents: malware or ransomware, account compromise, data exposure, lost devices, and service outages caused by attack.

## 2. Roles and contacts

| Role | Person | Phone | Backup |
|---|---|---|---|
| Incident lead (decision maker) | [NAME] | [PHONE] | [NAME] |
| Technical responder (IT) | [NAME / MSP] | [PHONE] | [NAME] |
| Communications / customer contact | [NAME] | [PHONE] | [NAME] |
| Legal counsel | [FIRM] | [PHONE] | |
| Cyber insurance carrier | [CARRIER, POLICY #] | [24/7 CLAIMS LINE] | |
| Law enforcement / reporting | local police, [FBI IC3 for US cyber crime] | | |

Keep a printed copy of this page. It must be reachable when systems are down.

## 3. Severity levels

| Level | Definition | Example | Response |
|---|---|---|---|
| 1 Critical | Business stopped or sensitive data confirmed exposed | ransomware, confirmed data theft | Immediate, notify owner and insurer |
| 2 High | Likely compromise, limited spread | compromised email account | Same day |
| 3 Medium | Contained or suspected | malware blocked, phishing clicked with no credentials entered | Within 1 business day |
| 4 Low | Policy or minor event | lost encrypted laptop | Normal handling |

## 4. Response phases

### Detect and report
Anyone who notices something unusual reports it to [IT CONTACT]. Record who, what, when, and what was observed.

### Triage
The incident lead and technical responder confirm whether it is real, assign a severity, and start an incident log (a running timeline with times).

### Contain
- Isolate affected devices from the network (unplug or disable Wi-Fi; do **not** power off unless advised, as memory may hold evidence)
- Disable or reset compromised accounts and revoke sessions
- Block malicious senders, domains, or IPs
- Preserve evidence: do not wipe or reimage until the lead agrees

### Eradicate
Remove malware, backdoors and malicious configuration (rules, forwarding, rogue accounts); patch the vulnerability that allowed entry.

### Recover
Restore from known-good backups; rebuild compromised systems; reset credentials; monitor closely for recurrence before declaring recovery complete.

### Communicate
- Staff: what to do and not do
- Customers/partners: only through the designated communications contact, with facts and no speculation
- Regulators/insurer: the incident lead decides with legal counsel; some laws impose strict notification deadlines

### Lessons learned
Within [two weeks] hold a blameless review: timeline, root cause, what worked, what failed, actions with owners and dates.

## 5. Scenario quick guides

**Ransomware:** isolate affected machines at once; do not pay or contact attackers without the incident lead, counsel and insurer; identify scope; restore from offline or immutable backups.

**Compromised email account:** reset password, revoke sessions, check mailbox rules and MFA methods, review sent mail, warn recipients of any fraudulent messages.

**Lost or stolen device:** confirm encryption, remote lock/wipe, reset credentials used on it, report to police if stolen.

**Accidental data disclosure:** retrieve or recall where possible, assess what was exposed and to whom, involve the incident lead.

## 6. Testing

Run a tabletop exercise (walk through a scenario on paper) at least [yearly]. Test backup restores quarterly.

## Appendix: incident log template

| Time | Who | Action or observation |
|---|---|---|
| | | |
