# Configuration snippets may be placed in this directo                                                                                                                  ry as well
includedir /etc/krb5.conf.d/

[logging]
 default = FILE:/var/log/krb5libs.log
 kdc = FILE:/var/log/krb5kdc.log
 admin_server = FILE:/var/log/kadmind.log

[libdefaults]
 default_realm = ANGELOP.HQ
 dns_lookup_realm = false
 dns_lookup_kdc = false
 ticket_lifetime = 24h
 renew_lifetime = 7d
 forwardable = true
 udp_preference_limit = 1
 default_tgs_enctypes = arcfour-hmac
 default_tkt_enctypes = arcfour-hmac

[realms]
  ANGELOP.HQ = {
  kdc = nodo2.angel.com
  admin_server = nodo2.angel.com
 }

[domain_realm]
   .angel.com = ANGELOP.HQ
   angel.com = ANGELOP.HQ

