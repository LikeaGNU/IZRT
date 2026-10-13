# **Handlab**

## Różnice między instrukcją a implementacją w PT

### Sprzęt

|Element|Instrukcja|PT|
|-|-|-|
|BRANCH1|Seria 8200L|PT8200|
|BRANCH2|Seria 8200L|PT8200|
|S1|Seria 9200L|IE-9320|
|S2|Seria 1000L|IE-9320|

#### Dołączone moduły

|Element|Intefejs|Nazwa modułu|
|-|-|-|
|S1|G1/0/1|GLC-TE|
|S1|G1/0/11|GLC-TE|
|S1|Zasilacz|9320 AC Power Supply|
|S2|G1/0/1|GLC-TE|
|S2|G1/0/11|GLC-TE|
|S2|Zasilacz|9320 AC Power Supply|
|BRANCH1|G0/0/2|GLC-TE|
|BRANCH2|G0/0/2|GLC-TE|

### Uwagi

BRANCH1 i BRANCH2 nie rozpoznają polecenia ``mtu 1476``.
```
! Konfiguracja tunelu VPN
int Tunnel1
no ip addr

! % Invalid input detected at '^' marker.
mtu 1476

ipv6 addr 2001:DB8:ACAD:12::1/64
tunnel mode ipv6ip
tunnel source g0/0/2
tunnel dest 209.165.200.2
exit
```
