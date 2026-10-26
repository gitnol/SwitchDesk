# Security Policy

SwitchDesk stores admin credentials for network switches and can change their configuration, update their firmware and reboot them. Security reports are very welcome.

## Supported versions

Only the latest release gets security fixes. There are no backports to older versions. SwitchDesk tells you when a new release is out (yellow bar at the top, or **Settings → Check for updates**).

| Version | Supported |
| ------- | --------- |
| Latest release (currently 0.8.x) | ✅ |
| Anything older | ❌ please update |

## Reporting a vulnerability

**Please don't report security issues in public issues or Discussions.**

Report them privately through GitHub instead: **[Report a vulnerability](https://github.com/jaba0x/SwitchDesk/security/advisories/new)** (Security tab → *Report a vulnerability*).

Please include:

- the SwitchDesk version and OS (macOS / Windows),
- the switch family involved, if any (AOS-CX, AOS-S, Instant On local/cloud),
- the steps to reproduce, or the affected file and line,
- what an attacker needs (local access, a crafted file, a position in the network) and what they gain.

Please don't include real passwords, configs or IP addresses from your network. Redact them or use test values.

## What to expect

SwitchDesk is maintained by one person in their spare time. These are goals, not guarantees:

- a reply within **7 days**,
- an assessment and a rough plan within **14 days**,
- a fixed release as soon as possible, usually within **30 days** for high-severity issues.

If the report is accepted, the fix ships in a new release with a GitHub Security Advisory. You are credited unless you'd rather not be. If it is declined, you get an explanation.

Please give us a chance to ship a fix before you publish details. 90 days is the usual upper limit.

## Scope

In scope, for example:

- credential storage and the `.sdbak` export/import,
- connections to switches (SSH, HTTPS/REST, Instant On web interface and portal), including certificate and host-key checks,
- firmware handling (library, downloads, upload, built-in TFTP server),
- the app UI and its bindings (e.g. script injection through switch data or imported files),
- the build and release workflow in `.github/workflows`.

Out of scope:

- vulnerabilities in the switches or their firmware. Report those to HPE Aruba Networking,
- attacks that need full control of the user's computer or account,
- the missing Apple notarization and Windows code signing (known, see the release notes),
- the documentation site and landing page, unless they affect users of the app.
