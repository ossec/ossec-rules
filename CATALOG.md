# Rules and decoder catalog

Index of every rule file and decoder file in this repository.
Rule ids are unique across `rules.d/`. A range is the lowest and highest id in that file, not a promise that every number in between is used.
Search this file for a product name, a rule id, or a decoder name, then open the path in the same row.

## Rules

| File | Rule ids | Rules | Group |
| --- | --- | ---: | --- |
| `rules.d/00-crs-rules_config.xml` | 1-7 | 7 | syslog |
| `rules.d/00-crs-syslog_rules.xml` | 1001-10100 | 99 | syslog,errors |
| `rules.d/50-crs-apache_rules.xml` | 30100-30411 | 43 | apache |
| `rules.d/50-crs-apparmor_rules.xml` | 52000-52004 | 5 | local,syslog,apparmor |
| `rules.d/50-crs-arpwatch_rules.xml` | 7200-7209 | 10 | syslog,arpwatch |
| `rules.d/50-crs-asterisk_rules.xml` | 6200-6258 | 16 | syslog,asterisk |
| `rules.d/50-crs-cimserver_rules.xml` | 9600-9611 | 3 | syslog,cimserver |
| `rules.d/50-crs-cisco-ios_rules.xml` | 4700-4724 | 12 | syslog,cisco_ios |
| `rules.d/50-crs-clam_av_rules.xml` | 52500-52509 | 10 | clamd,freshclam |
| `rules.d/50-crs-courier_rules.xml` | 3900-3911 | 7 | syslog,courier |
| `rules.d/50-crs-cpanel_rules.xml` | 11000-11006 | 7 | syslog,cpanel |
| `rules.d/50-crs-dnsmasq_rules.xml` | 53551 | 1 | local,dns,dnsmasq |
| `rules.d/50-crs-dovecot_rules.xml` | 9700-9771 | 12 | dovecot |
| `rules.d/50-crs-dropbear_rules.xml` | 51000-51093 | 13 | syslog,sshd,dropbear |
| `rules.d/50-crs-exim_rules.xml` | 13000-13010 | 7 | exim |
| `rules.d/50-crs-firewall_rules.xml` | 4100-4151 | 4 | firewall |
| `rules.d/50-crs-firewalld_rules.xml` | 40900-40903 | 4 | local,firewalld |
| `rules.d/50-crs-ftpd_rules.xml` | 11100-11113 | 14 | syslog,ftpd |
| `rules.d/50-crs-hordeimp_rules.xml` | 9300-9352 | 9 | syslog,hordeimp |
| `rules.d/50-crs-ids_rules.xml` | 20100-20162 | 8 | ids |
| `rules.d/50-crs-imapd_rules.xml` | 3600-3651 | 5 | syslog,imapd |
| `rules.d/50-crs-kesl_rules.xml` | 53801-53817 | 17 | kesl |
| `rules.d/50-crs-lighttpd_rules.xml` | 56201 | 1 | local,lighttpd |
| `rules.d/50-crs-linux_usbdetect_rules.xml` | 53600-53604 | 5 | linux, usb |
| `rules.d/50-crs-mailscanner_rules.xml` | 3700-3752 | 5 | syslog,mailscanner |
| `rules.d/50-crs-mhn_cowrie_rules.xml` | 53830-53832 | 3 | mhn,json |
| `rules.d/50-crs-mhn_dionaea_rules.xml` | 53826 | 1 | mhn,json |
| `rules.d/50-crs-ms-exchange_rules.xml` | 3800-3852 | 5 | ms,exchange |
| `rules.d/50-crs-ms_dhcp_rules.xml` | 6300-6376 | 49 | windows,dhcp |
| `rules.d/50-crs-ms_ftpd_rules.xml` | 11500-11512 | 8 | syslog,msftp |
| `rules.d/50-crs-msauth_rules.xml` | 18100-18261 | 124 | windows |
| `rules.d/50-crs-mysql_rules.xml` | 50100-50180 | 10 | mysql_log |
| `rules.d/50-crs-named_rules.xml` | 12100-12149 | 49 | syslog,named |
| `rules.d/50-crs-netscreenfw_rules.xml` | 4500-4560 | 16 | netscreenfw |
| `rules.d/50-crs-nginx_rules.xml` | 31300-31320 | 11 | apache |
| `rules.d/50-crs-openbsd_rules.xml` | 51500-51560 | 47 | local,syslog,openbsd |
| `rules.d/50-crs-opensmtpd_rules.xml` | 53500-53508 | 9 | syslog,smtpd |
| `rules.d/50-crs-ossec_rules.xml` | 500-701 | 46 | ossec |
| `rules.d/50-crs-pam_rules.xml` | 5500-5557 | 15 | pam,syslog |
| `rules.d/50-crs-php_rules.xml` | 31401-31430 | 13 | apache |
| `rules.d/50-crs-pix_rules.xml` | 4300-4386 | 33 | syslog,pix |
| `rules.d/50-crs-postfix_rules.xml` | 3300-3390 | 23 | syslog,postfix |
| `rules.d/50-crs-postgresql_rules.xml` | 50500-50581 | 13 | postgresql_log |
| `rules.d/50-crs-proftpd_rules.xml` | 11200-11253 | 26 | syslog,proftpd |
| `rules.d/50-crs-pure-ftpd_rules.xml` | 11300-11312 | 12 | syslog,pure-ftpd |
| `rules.d/50-crs-racoon_rules.xml` | 14100-14151 | 10 | syslog,racoon |
| `rules.d/50-crs-roundcube_rules.xml` | 9400-9403 | 4 | syslog,roundcube |
| `rules.d/50-crs-sendmail_rules.xml` | 3100-3191 | 19 | syslog,sendmail |
| `rules.d/50-crs-smbd_rules.xml` | 13100-13112 | 12 | syslog,smbd |
| `rules.d/50-crs-solaris_bsm_rules.xml` | 6100-6106 | 7 | syslog,solaris_bsm |
| `rules.d/50-crs-sonicwall_rules.xml` | 4800-4851 | 12 | syslog,sonicwall |
| `rules.d/50-crs-spamd_rules.xml` | 3500-3502 | 3 | syslog,spamd |
| `rules.d/50-crs-squid_rules.xml` | 35000-35095 | 22 | squid |
| `rules.d/50-crs-sshd_rules.xml` | 5700-5758 | 58 | syslog,sshd |
| `rules.d/50-crs-symantec-av_rules.xml` | 7300-7320 | 4 | symantec |
| `rules.d/50-crs-symantec-ws_rules.xml` | 7400-7425 | 5 | symantec |
| `rules.d/50-crs-sysmon_rules.xml` | 18501-18602 | 24 | sysmon_process-anomalies |
| `rules.d/50-crs-systemd_rules.xml` | 40700-40703 | 4 | local,systemd |
| `rules.d/50-crs-telnetd_rules.xml` | 5600-5631 | 6 | syslog,telnetd |
| `rules.d/50-crs-trend-osce_rules.xml` | 7600-7613 | 5 | trend_micro,ocse |
| `rules.d/50-crs-unbound_rules.xml` | 53760-53775 | 9 | syslog,unbound |
| `rules.d/50-crs-vmpop3d_rules.xml` | 9800-9820 | 3 | syslog,vm-pop3d |
| `rules.d/50-crs-vmware_rules.xml` | 19100-19153 | 20 | vmware |
| `rules.d/50-crs-vpn_concentrator_rules.xml` | 14200-14251 | 5 | syslog,cisco_vpn |
| `rules.d/50-crs-vpopmail_rules.xml` | 9900-9953 | 8 | syslog,vpopmail |
| `rules.d/50-crs-vsftpd_rules.xml` | 11400-11452 | 7 | syslog,vsftpd |
| `rules.d/50-crs-web_rules.xml` | 31100-31165 | 26 | web,accesslog |
| `rules.d/50-crs-wordpress_rules.xml` | 9500-9551 | 8 | syslog,wordpress |
| `rules.d/50-crs-zeus_rules.xml` | 31200-31251 | 8 | zeus |
| `rules.d/55-crs-msft-firewall_rules.xml` | 53631-53654 | 24 | windows,firewall |
| `rules.d/55-crs-topleveldomain_rules.xml` | 31111 | 1 | web-access |
| `rules.d/60-crs-attack_rules.xml` | 40101-40601 | 13 | syslog,attacks |
| `rules.d/60-crs-mcafee_av_rules.xml` | 7500-7550 | 16 | mcafee |
| `rules.d/60-crs-ms-se_rules.xml` | 7701-7751 | 17 | windows,mse |
| `rules.d/60-crs-ms1016_usbdetect_rules.xml` | 53626 | 1 | windows,usb |
| `rules.d/60-crs-msft-ipsec_rules.xml` | 18651-18668 | 18 | windows, ipsec |
| `rules.d/60-crs-msft-powershell_rules.xml` | 20500-20505 | 6 | windows,powershell |
| `rules.d/60-crs-web_appsec_rules.xml` | 31501-31550 | 20 | web,appsec,attack |
| `rules.d/70-crs-last_rootlogin_rules.xml` | 25000 | 1 | access-control |
| `rules.d/70-crs-nsd_rules.xml` | 53200-53212 | 13 | syslog,dns,nsd |
| `rules.d/70-crs-openbsd-dhcp_rules.xml` | 53000-53013 | 12 | syslog,dhcpd |
| `rules.d/70-crs-owncloud_rules.xml` | 53300-53308 | 9 | syslog,owncloud |
| `rules.d/70-crs-proxmox-ve_rules.xml` | 53400-53403 | 4 | syslog,proxmox-ve |
| `rules.d/70-crs-psad_rules.xml` | 53700-53716 | 9 | syslog,psad |
| `rules.d/99-crs-policy_rules.xml` | 17101-17102 | 2 | policy_violation |

## Decoders

The parent decoder `name` is what a rule selects with `<decoded_as>`. Child decoder names extract fields from that parent.

| File | Decoder names |
| --- | --- |
| `decoders.d/00-crs-iptables_decoder.xml` | `iptables`, `iptables-1`, `iptables-2`, `iptables-shorewall`, `iptables-shorewall2` |
| `decoders.d/00-crs-pam_decoder.xml` | `pam`, `pam-user`, `pam-user2`, `pam-host-user`, `pam-ruser`, `pam-host` |
| `decoders.d/00-crs-windows-date-format_decoder.xml` | `windows-date-format` |
| `decoders.d/50-crs-aix-ipsec_decoder.xml` | `aix-ipsec` |
| `decoders.d/50-crs-apache_decoder.xml` | `apache-errorlog`, `apache24-errorlog-ip-port`, `apache24-errorlog-ip`, `apache-errorlog-ip` |
| `decoders.d/50-crs-apparmor_decoder.xml` | `apparmor` |
| `decoders.d/50-crs-arpwatch_decoder.xml` | `arpwatch`, `arpwatch-new` |
| `decoders.d/50-crs-asterisk_decoder.xml` | `asterisk`, `asterisk-hijacking`, `asterisk-denied`, `asterisk-denied2`, `asterisk-denied3-ipv6`, `asterisk-denied3`, `asterisk-iax-authentication-denied` |
| `decoders.d/50-crs-auditd_decoder.xml` | `auditd`, `auditd-selinux`, `auditd-syscall`, `auditd-config`, `auditd-path`, `auditd-user` |
| `decoders.d/50-crs-barracuda_decoder.xml` | `barracuda-svf-email`, `barracuda-svf1`, `barracuda-svf-admin`, `barracuda-svf-admin-change`, `barracuda-svf-admin-auth` |
| `decoders.d/50-crs-checkpoint_decoder.xml` | `checkpoint-syslog`, `checkpoint-syslog-fw`, `checkpoint-syslog-ids` |
| `decoders.d/50-crs-chkpwd_decoder.xml` | `unix_chkpwd`, `chkpwd-user` |
| `decoders.d/50-crs-cimserver_decoder.xml` | `cimserver`, `cimserver-failed-authentication` |
| `decoders.d/50-crs-cisco-ios_decoder.xml` | `cisco-ios`, `cisco-ios-acl`, `cisco-ios-ids`, `cisco-ios-generic` |
| `decoders.d/50-crs-cisco-vpnconcentrator_decoder.xml` | `cisco-vpn-concentrator` |
| `decoders.d/50-crs-clamd_decoder.xml` | `clamd`, `freshclam` |
| `decoders.d/50-crs-courier_decoder.xml` | `courier`, `courier-login`, `courier-generic` |
| `decoders.d/50-crs-cpanel_decoder.xml` | `cpanel`, `cpanel-login-failed`, `cpanel-login-success`, `cpanel-session-new`, `cpanel-session-logout`, `cpanel-access-failed` |
| `decoders.d/50-crs-dhcp_decoder.xml` | `dhcpd`, `dhcpd-data`, `dhcpd-ack`, `dhcpd-release` |
| `decoders.d/50-crs-dnsmasq_decoder.xml` | `dnsmasq`, `dnsmasq2` |
| `decoders.d/50-crs-doas_decoder.xml` | `doas`, `doas-user` |
| `decoders.d/50-crs-dovecot_decoder.xml` | `dovecot`, `dovecot-success`, `dovecot-aborted`, `dovecot-fail`, `dovecot-authfailed`, `dovecot-disconnect`, `dovecot-info`, `imap-login-login`, `dovecot-info-auth` |
| `decoders.d/50-crs-dragon_decoder.xml` | `dragon-nids` |
| `decoders.d/50-crs-dropbear_decoder.xml` | `dropbear`, `dropbear-bad-password`, `dropbear-nonexist`, `dropbear-from` |
| `decoders.d/50-crs-exim_decoder.xml` | `exim-authfailed`, `exim-connect`, `exim-disconnect`, `exim-syntax-errors` |
| `decoders.d/50-crs-ftpd_decoder.xml` | `ftpd`, `ftpd-mac-failure`, `ftpd-refused`, `ftpd-ip`, `ftpd-tru64` |
| `decoders.d/50-crs-grandstream_decoder.xml` | `grandstream-ata`, `grandstream-registration`, `grandstream-fts-registered`, `grandstream-incoming-cid`, `grandstream-outgoing-call` |
| `decoders.d/50-crs-horde_decoder.xml` | `horde_imp`, `horde_imp_success`, `horde_imp_failed` |
| `decoders.d/50-crs-imapd_decoder.xml` | `imapd` |
| `decoders.d/50-crs-ipfilter_decoder.xml` | `ipfilter` |
| `decoders.d/50-crs-isakmpd_decoder.xml` | `isakmpd`, `isakmpd-from`, `isakmpd-peer` |
| `decoders.d/50-crs-lighttpd_decoder.xml` | `lighttpd` |
| `decoders.d/50-crs-mailscanner_decoder.xml` | `mailscanner`, `mailscanner-ip` |
| `decoders.d/50-crs-mptscsi_decoder.xml` | `mptscsih-1`, `mptbase-1` |
| `decoders.d/50-crs-ms-dhcp_decoder.xml` | `ms-dhcp-ipv4`, `ms-dhcp-ipv6` |
| `decoders.d/50-crs-mysql_decoder.xml` | `mysql_log` |
| `decoders.d/50-crs-named_decoder.xml` | `named`, `named-query`, `named_client`, `named_from`, `named-master` |
| `decoders.d/50-crs-netscreen_decoder.xml` | `netscreenfw`, `netscreenfw-traffic`, `netscreenfw-critical`, `netscreenfw-admin` |
| `decoders.d/50-crs-nginx_decoder.xml` | `nginx-errorlog`, `nginx-errorlog-ip` |
| `decoders.d/50-crs-nsd_decoder.xml` | `nsd`, `nsd-from` |
| `decoders.d/50-crs-ntpd_decoder.xml` | `ntpd`, `ntpd-bad-peer`, `ntpd-recvmsg` |
| `decoders.d/50-crs-openbsd-pf_decoder.xml` | `pf` |
| `decoders.d/50-crs-openbsd_decoder.xml` | `bsd_kernel`, `bsd_arp`, `open-userdel`, `mountd`, `mountd-host`, `nss-ldap`, `ldap-server`, `groupdel`, `openbsd-httpd` |
| `decoders.d/50-crs-openldap_decoder.xml` | `openldap`, `openldap-connect`, `openldap-bind`, `openldap-result` |
| `decoders.d/50-crs-opensmtpd_decoder.xml` | `smtpd`, `smtpd-client`, `smtpd-relay`, `smtpd-in` |
| `decoders.d/50-crs-ossec_decoder.xml` | `ossec`, `ossec-logcollector`, `ossec-agent`, `ossec-alert1`, `ossec-alert`, `ar_log` |
| `decoders.d/50-crs-owncloud_decoder.xml` | `owncloud`, `owncloud-failed1`, `owncloud-failed2`, `owncloud-malicious`, `owncloud-loglevel` |
| `decoders.d/50-crs-pix_decoder.xml` | `pix`, `pix-fw1`, `pix-fw2`, `pix-fw3`, `pix-fw4`, `pix-fw5`, `pix-fw6`, `pix-fw7`, `pix-fw8`, `pix-url-success`, `pix-url-deny`, `pix-attacks`, `pix-srcip`, `pix-srcip-port`, `pix-generic` |
| `decoders.d/50-crs-portsentry_decoder.xml` | `portsentry`, `portsentry-attackalert`, `portsentry-blocked` |
| `decoders.d/50-crs-postfix_decoder.xml` | `postfix`, `postfix-reject`, `postfix-sasl`, `postfix-connect-abort` |
| `decoders.d/50-crs-postgresql_decoder.xml` | `postgresql_log` |
| `decoders.d/50-crs-proftpd_decoder.xml` | `proftpd`, `proftpd-success`, `proftpd-ip` |
| `decoders.d/50-crs-proxmox_decoder.xml` | `pvedaemon`, `pvestatd`, `pveproxy`, `pvepw-logger`, `pvedaemon-auth-failed`, `pvedaemon-auth-success` |
| `decoders.d/50-crs-psad_decoder.xml` | `psad`, `psad-scan`, `psad-repeated`, `psad-signature` |
| `decoders.d/50-crs-pure-ftpd_decoder.xml` | `pure-ftpd`, `pure-ftpd-login`, `pure-ftpd-generic`, `pure-transfer` |
| `decoders.d/50-crs-raccoon_decoder.xml` | `racoon`, `racoon-failed`, `racoon-action` |
| `decoders.d/50-crs-roundcube_decoder.xml` | `roundcube`, `roundcube-success`, `roundcube-denied-old`, `roundcube-denied-new` |
| `decoders.d/50-crs-rshd_decoder.xml` | `rshd`, `rshd-illegal-connection` |
| `decoders.d/50-crs-sendmail_decoder.xml` | `sendmail-reject`, `sendmail-pre-greeting`, `sendmail-reject-nodns`, `sendmail-reject-dns`, `smf-sav-reject` |
| `decoders.d/50-crs-smbd_decoder.xml` | `smbd`, `smbd-user`, `smbd-ip`, `smbd-from`, `smbd-client`, `nmbd` |
| `decoders.d/50-crs-snort_decoder.xml` | `snort`, `snort2` |
| `decoders.d/50-crs-solaris-bsm_decoder.xml` | `solaris_bsm`, `solaris_bsm_session` |
| `decoders.d/50-crs-sonicwall_decoder.xml` | `sonicwall` |
| `decoders.d/50-crs-squid_decoder.xml` | `squid-accesslog` |
| `decoders.d/50-crs-sshd_decoder.xml` | `sshd`, `sshd-success`, `ssh-denied`, `sshd-success-solaris`, `ssh-kbd`, `ssh-invfailed`, `ssh-failed`, `ssh-error`, `ssh-pam-error`, `ssh-reverse-mapping`, `ssh-invalid-user`, `ssh-scan`, `ssh-received`, `ssh-disconnected`, `ssh-connection`, `ssh-negotiate`, `ssh-protocol`, `ssh-scan2`, `ssh-osx-refuse`, `ssh-closed`, `ssh-disconnect`, `ssh-pam`, `ssh-connect-to`, `sshd-ldap`, `sshd-negotiate`, `sshd-pam-host-user`, `sshd-invalid`, `sshd-exceed` |
| `decoders.d/50-crs-su_decoder.xml` | `su`, `su-detail`, `su-ldap`, `su-failed`, `su-detail2` |
| `decoders.d/50-crs-sudo_decoder.xml` | `sudo` |
| `decoders.d/50-crs-suhosin_decoder.xml` | `suhosin` |
| `decoders.d/50-crs-symantec-av_decoder.xml` | `symantec-av` |
| `decoders.d/50-crs-symantec-websecurity_decoder.xml` | `symantec-websecurity` |
| `decoders.d/50-crs-sysmon_decoder.xml` | `Sysmon-EventID#1` |
| `decoders.d/50-crs-telnetd_decoder.xml` | `telnetd`, `telnetd-ip` |
| `decoders.d/50-crs-trend-osce_decoder.xml` | `trend-osce` |
| `decoders.d/50-crs-unbound_decoder.xml` | `unbound`, `unbound-a` |
| `decoders.d/50-crs-vm-pop3d_decoder.xml` | `vm-pop3d`, `vm-pop3d-fail` |
| `decoders.d/50-crs-vmware-esx_decoder.xml` | `vmware`, `vmware-extra`, `vmware-syslog`, `vmware-success`, `vmware-login` |
| `decoders.d/50-crs-vpopmail_decoder.xml` | `vpopmail`, `vpopmail-fail`, `vpopmail-notfound`, `vpopmail-empty`, `vpopmail-success` |
| `decoders.d/50-crs-vsftpd_decoder.xml` | `vsftpd`, `vsftpd_login`, `vsftpd_connect`, `vsftpd_cmd`, `vsftpd_default` |
| `decoders.d/50-crs-web-accesslog_decoder.xml` | `web-accesslog` |
| `decoders.d/50-crs-windows-ntsyslog_decoder.xml` | `windows-ntsyslog` |
| `decoders.d/50-crs-windows-snare_decoder.xml` | `windows-snare` |
| `decoders.d/50-crs-windows_decoder.xml` | `windows`, `windows1` |
| `decoders.d/50-crs-wordpress_decoder.xml` | `wordpress` |
| `decoders.d/50-crs-zeus_decoder.xml` | `zeus` |
| `decoders.d/60-crs-cowrie_decoder.xml` | `cowrie`, `cowrie-attempt`, `cowrie-session`, `cowrie-command` |
| `decoders.d/60-crs-dionaea_decoder.xml` | `dionaea` |
| `decoders.d/60-crs-iis-ftp_decoder.xml` | `msftp` |
| `decoders.d/60-crs-iis-smtp_decoder.xml` | `msexchange` |
| `decoders.d/60-crs-iis-web_decoder.xml` | `web-accesslog-iis5`, `web-accesslog-iis6`, `web-accesslog-iis-default` |
| `decoders.d/60-crs-kaspersky_decoder.xml` | `kesl`, `kesl-avbases-old`, `kesl-threat-detected`, `kesl-taskstatechange` |
| `decoders.d/60-crs-windows-firewall_decoder.xml` | `windows-firewall` |

