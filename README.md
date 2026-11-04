# OSSEC Rules

Community rules and decoders for [OSSEC HIDS](https://github.com/ossec/ossec-hids). Each product is one XML file under `rules.d/` or `decoders.d/`. The `crs` prefix on those filenames means this community ruleset.

Look up a rule id, a decoder name, or a product in [CATALOG.md](CATALOG.md). Release history is in [CHANGELOG.md](CHANGELOG.md). Decoder field names are in [decoders.d/README.md](decoders.d/README.md).

## Layout

| Path | Contents |
| --- | --- |
| `rules.d/` | Alert rules. `{order}-crs-{product}_rules.xml`. A rule id appears in exactly one file. |
| `decoders.d/` | Log decoders. `{order}-crs-{product}_decoder.xml`. |
| `ossec-testing/tests/` | Sample logs. `{product}.ini` records the rule id, alert level, and decoder each line must hit. |
| `shared/` | Rootcheck file lists and CIS/ACSC `.rcl.txt` audit policies. Added in 3.0. |

The numeric prefix is load order, not a severity:

| Prefix | Role |
| --- | --- |
| `00` | Syslog base rules and the generic rule template |
| `50` | Product rules and decoders |
| `55` | Windows firewall and a small URL overlay |
| `60` | Attack signatures, web appsec, and host security products |
| `70` | Later product packs (NSD, dhcpd, ownCloud, Proxmox, PSAD) |
| `99` | Time-of-day login policy |

## Find a rule or a decoder

- Rule id: search `rules.d` for `id="5714"`, or find the range in [CATALOG.md](CATALOG.md).
- Product: the filename contains it. SSH is `rules.d/50-crs-sshd_rules.xml` and `decoders.d/50-crs-sshd_decoder.xml`.
- Log line: `ossec-testing/tests/<product>.ini`.
- Decoder name: search `decoders.d` for `<decoder name="sshd-success">`. Rules select the parent decoder with `<decoded_as>`.

## Install

Copy the files into an OSSEC tree that loads directories:

```
rules.d/*.xml     -> /var/ossec/etc/rules.d/
decoders.d/*.xml  -> /var/ossec/etc/decoders.d/
shared/*          -> /var/ossec/etc/shared/
```

`ossec.conf` needs the directory stanzas. Per-file `<include>` entries do not load these paths.

```xml
<rules>
  <decoder_dir pattern=".xml$">etc/decoders.d</decoder_dir>
  <rule_dir pattern=".xml$">etc/rules.d</rule_dir>
</rules>
```

## Tests

`ossec-testing/runtests.py` feeds each `log` line to `ossec-logtest`. Run it on a host where OSSEC is installed and these rules are the ones loaded. From `ossec-testing/`:

```
python runtests.py
python runtests.py sshd.ini
```

An `.ini` section has `rule`, `alert`, and `decoder`. A key named `log N pass` must match that rule. A key named `log N fail` must not.

## Releases

Tags on this repository: `v1.0`, `v2.0`, `v3.0`. The next release is 4.0. See [CHANGELOG.md](CHANGELOG.md).

## Changing a rule

Keep an existing rule id when the meaning stays the same. Add the log line that motivated the change under `ossec-testing/tests/`. A new id must not repeat one already listed in [CATALOG.md](CATALOG.md). Keep a decoder `name` stable when rules already select it.
