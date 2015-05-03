# LDAP mangle id

#### Overview
  Start a LDAP proxy server which relays queries to a real LDAP server but
  mangles uid and gid value of the posix accounts by adding or subtracting a
  value to them on the fly.

#### Use cases
  LDAP mangle id was written to be used with sssd, in order to allow enforcing distinct intervals of ids, as required for a multi-domain sssd configuration (see min_id/max_id in sssd.conf).
  
#### Code
  ldap-mangle-id is written in Perl, using the Net::LDAP modules.
  
#### Known alternatives
1.  https://github.com/mcavage/node-ldapjs
2.  https://github.com/pfmooney/node-ldapjs-mangle-proxy
