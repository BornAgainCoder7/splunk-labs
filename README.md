Splunk Labs

This repository contains SPL (Search Processing Language) queries for detecting security incidents using Splunk.

Detection Queries

`failed-logins.spl`

Detects multiple failed login attempts from the same source IP and username.

- Event Code: 4625
- Fields used: `user`, `src_ip`
- Purpose: Identify brute-force attacks or misconfigured systems causing login failures.

`account-lockouts.spl`

Detects user account lockouts, grouped by domain controller and source workstation.

- Event Code:** 4740
- Fields used: `TargetUserName`, `Caller_Computer_Name`, `host`
- Purpose: Investigate repeated lockouts, which could indicate misconfigurations or attacks.

Notes

- You can run these queries in Splunk Enterprise or Splunk Free if WinEventLogs are ingested.
- Field names are normalized for readability in dashboards and reports.

All queries are created and maintained for learning and security detection practice.

