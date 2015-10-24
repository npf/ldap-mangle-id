# LDAP mangle id

#### Overview
  Start a LDAP proxy server which relays queries to a real LDAP server with
  mangling uid and gid returned values for the posix accounts, by doing some arithmetic to them on the fly (e.g. uid+=const).

#### Use cases
  LDAP mangle id was written to be used with sssd, in order to allow enforcing distinct ranges of uid and gid values, as required for a multi-domain sssd configuration with overlapping uid/gid values (see min_id/max_id in sssd.conf).
  
#### Code
  ldap-mangle-id is written in Perl, using the Net::LDAP modules.
  
#### Possible alternatives
*   See: http://people.redhat.com/mskinner/rhug/q1.2014/Integrating-RHEL-and-LDAP.pdf
  *  https://github.com/mcavage/node-ldapjs
  *  https://github.com/pfmooney/node-ldapjs-mangle-proxy
  *  Openldap overlays, slapd-rwm
*  https://lists.fedorahosted.org/pipermail/sssd-users/2015-August/003357.html
