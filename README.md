# Day 11 - Network Access Control & Fail2Ban

> Day 11 of 14 in the **Zero to Production Infrastructure & Security** series.

Automated IP ban rules triggered by failed SSH logins and API abuse patterns.

| | |
|---|---|
| **Day** | 11 of 14 |
| **Status** | Under construction |
| **Verification** | `bash -n actions/ban-ip.sh actions/unban-ip.sh` |
| **Tags** | `fail2ban`  `iptables`  `security`  `intrusion-prevention`  `linux` |

## Focus

- Active response scripting
- Firewall rule automation
- Intrusion prevention feedback loops
- Ban escalation and unban tooling

## Status

Implementation lands during the Day 11 build session. Until then this
repository holds the agreed structure only - there is no placeholder code here
pretending to work.

The nightly pipeline appends the real verification result to [STATUS.md](STATUS.md).

## Layout

```
11-fail2ban-active-response/
  README.md        this file
  LICENSE          MIT
  STATUS.md        machine-written verification record
  .gitignore       shared from the series root
  .gitattributes   forces LF endings so bash scripts run on Windows
```

## Verify

```bash
bash -n actions/ban-ip.sh actions/unban-ip.sh
```

The nightly job at 22:00 runs this command, records the result and
exit code in STATUS.md, then tags and pushes the repository.

## Licence

MIT. See [LICENSE](LICENSE).