[libdefaults]
default_realm = SEBC.COM
dns_lookup_kdc = false
dns_lookup_realm = false
ticket_lifetime = 86400
renew_lifetime = 604800
forwardable = true
default_tgs_enctypes = aes256-cts
default_tkt_enctypes = aes256-cts
permitted_enctypes = aes256-cts
udp_preference_limit = 1
kdc_timeout = 3000
[realms]
SEBC.COM = {
kdc = ip-172-31-26-116.eu-central-1.compute.internal
admin_server = ip-172-31-26-116.eu-central-1.compute.internal
}
