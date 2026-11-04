# Changelog

Release history for the OSSEC community ruleset. Versions match the git tags on this repository. The ruleset uses the `crs` filename prefix (community ruleset).

## [4.0] - 2026-11-04

Rules and decoders accumulated since 3.0, kept in line with the matching ossec-hids fixes.

### Security

- Hardened the `windows1` and `barracuda-svf1` decoders against regular-expression denial of service (ANT-2026-7ME0G28I).

### New coverage

- cPanel login, session, and access-log authentication (rules 11000-11006), including `cpsrvd`, `webmaild`, `whostmgrd`, and `cpaneld`.
- Postfix SMTP connect aborts (`SSL_accept` and lost connection after `CONNECT`), with per-source escalation (rules 3335 and 3358).
- Snort fast alerts in drop mode (`[Drop]`) now reach the snort field decoder.
- Asterisk denied calls from IPv6 addresses that are not wrapped in square brackets. `srcip` is the address without brackets, so active response can use it.
- IIS W3C access logs now yield the client User-Agent, and `sc-status` stays on the status field.

### Fixes

- **dpkg.** Rule 2902 matches install, upgrade, and configure. Package removal no longer raises a false "installed" alert.
- **Windows / Microsoft auth.** Failed-logon 4625 decodes UPN account names, dots, and machine accounts ending in `$`, and it no longer treats a Subject dash as the account. Well-known group SID matches are anchored, so a RID such as `-51901` is not Enterprise Admins (`-519`). Universal-group member changes (4756/4757) chain through rules 18213-18215. Rootcheck ignores the Windows Application Experience `:Win32App_1` NTFS stream.
- **SSH.** Rule 5714 (CRC-32 compensation) fires from the compensation line after one corrupted-bytes alert, instead of waiting on rule 5713.
- **Postfix.** Rule 3331 no longer treats a postscreen client port as SMTP response 452. The decoder no longer stores that port as the queue id.
- **BIND.** Client lines with an optional `@cookie` prefix still expose `srcip`.
- **Dovecot.** A trailing comma after `lip=` is no longer part of `dstip`.
- **Web.** Rule 31110 (PHP CGI) is limited to `.php` and `cgi-bin` URLs. Rule 31508 adds `muhstik` and drops `MJ12bot`. Rule 31107 no longer suppresses attacks on CMS search URLs. Request URLs may contain spaces. CMS login rule 31509 is parented on 31100 so it does not hide POST flood and appsec rules. The dead Honeynet Project link on rule 40601 points at an archive snapshot.
- **ProFTPD.** `sreaddir` buffer growth during directory listings is ignored.
- **PostgreSQL / OpenBSD httpd.** Broader prematches were taking cPanel logs. Those decoders are narrower, and cPanel has its own decoder.
- **syslog.** Rule 40501 requires a higher frequency on the same location. Rule 532 ignores `df` 100% alerts for `/dev/loop` and `/snap`. Rule 52000 (AppArmor grouping) requires parent 5100. `yum.log` and syscheck-registry rules match with `location_pcre2`, because those paths are a location, not a hostname.

### Upgrade notes

- `location_pcre2` on the yum and syscheck-registry rules follows the agent-versus-log hostname split. Alerts that previously keyed off hostname for those files now key off the log path.
- SSH rule 5714 can alert after a single CRC-32 compensation event.
- Search-engine URLs that rule 31107 used to silence can now alert as web attacks.

## [3.0] - 2023-06-01

Rootcheck malware signatures and compliance audit lists under `shared/`.

## [2.0] - 2020-10-01

PCRE2 port of the rules, aligned with OSSEC main.

## [1.0] - 2020-09-08

Initial community ruleset. Legacy (non-PCRE2) rules.
