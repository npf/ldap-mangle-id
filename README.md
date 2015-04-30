# LDAP proxy mangle id

  Start a LDAP proxy which relays queries to a real LDAP server but mangles uid
  and gid value of the posix accounts by adding or subtracting a value to them.

  Can be used enforce distinct intervals of ids, as required for a multi-domain
  sssd configuration (see min_id/max_id in sssd.conf).
