# Jarkom-Modul-4-F10-2023
Laporan resmi praktikum modul 4 subnetting &amp; routing mata kuliah jaringan komputer

# Anggota
Kelompok: F10
Nama | NRP
--- | ---
Thoriq Afif Habibi | 5025211154
Radhiyan Muhammad Hisan | 5025211166

# Konfigurasi VLSM
![tree vlsm](./F10_Tree-VLSM.jpg)

## _Router_
### Aura
```
auto eth0
iface eth0 inet dhcp

# ke Denken
auto eth1
iface eth1 inet static
	address 192.226.0.37
	netmask 255.255.255.252

# ke Frieren
auto eth2
iface eth2 inet static
	address 192.226.0.1
	netmask 255.255.255.252

# ke Eisen
auto eth3
iface eth3 inet static
	address 192.226.0.17
	netmask 255.255.255.252
```

### Denken
```
# ke Aura
auto eth0
iface eth0 inet static
	address 192.226.0.38
	netmask 255.255.255.252
	gateway 192.226.0.37
    
# ke Switch2
auto eth1
iface eth1 inet static
	address 192.226.1.1
	netmask 255.255.255.0
```

### Frieren
```
# ke Aura
auto eth0
iface eth0 inet static
	address 192.226.0.2
	netmask 255.255.255.252
	gateway 192.226.0.1
    
# ke Switch3
auto eth1
iface eth1 inet static
	address 192.226.0.65
	netmask 255.255.255.224
    
# ke Flamme
auto eth2
iface eth2 inet static
	address 192.226.0.5
	netmask 255.255.255.252
```

### Flamme
```
# ke Frieren
auto eth0
iface eth0 inet static
	address 192.226.0.6
	netmask 255.255.255.252
	gateway 192.226.0.5
    
# ke Fern
auto eth1
iface eth1 inet static
	address 192.226.0.9
	netmask 255.255.255.252
    
# ke Switch5
auto eth2
iface eth2 inet static
	address 192.226.16.1
	netmask 255.255.252.0
    
# ke Himmel
auto eth3
iface eth3 inet static
	address 192.226.0.13
	netmask 255.255.255.252
```

### Fern
```
# ke Flamme
auto eth0
iface eth0 inet static
	address 192.226.0.10
	netmask 255.255.255.252
	gateway 192.226.0.9
    
# ke Switch4
auto eth1
iface eth1 inet static
	address 192.226.24.1
	netmask 255.255.248.0
```

### Himmel
```
# ke Flamme
auto eth0
iface eth0 inet static
	address 192.226.0.14
	netmask 255.255.255.252
	gateway 192.226.0.13
    
# ke Switch6
auto eth1
iface eth1 inet static
	address 192.226.0.49
	netmask 255.255.255.248
```

### Eisen
```
# ke Aura
auto eth0
iface eth0 inet static
	address 192.226.0.18
	netmask 255.255.255.252
	gateway 192.226.0.17

# ke Switch1
auto eth1
iface eth1 inet static
	address 192.226.0.41
	netmask 255.255.255.248

# ke Switch0
auto eth2
iface eth2 inet static
	address 192.226.0.33
	netmask 255.255.255.252

# ke Lugner
auto eth3
iface eth3 inet static
	address 192.226.0.29
	netmask 255.255.255.252

# ke Linie
auto eth4
iface eth4 inet static
	address 192.226.0.21
	netmask 255.255.255.252
```

### Lugner
```
# ke Eisen
auto eth0
iface eth0 inet static
	address 192.226.0.30
	netmask 255.255.255.252
	gateway 192.226.0.29
    
# ke Switch10
auto eth1
iface eth1 inet static
	address 192.226.12.1
	netmask 255.255.255.0
    
# ke Switch9
auto eth2
iface eth2 inet static
	address 192.226.2.1
	netmask 255.255.255.0
```

### Linie
```
# ke Eisen
auto eth0
iface eth0 inet static
	address 192.226.0.22
	netmask 255.255.255.252
	gateway 192.226.0.21
    
# ke Switch11
auto eth1
iface eth1 inet static
	address 192.226.4.1
	netmask 255.255.254.0
    
# ke Lawine
auto eth2
iface eth2 inet static
	address 192.226.0.25
	netmask 255.255.255.252
```

### Lawine
```
# ke Linie
auto eth0
iface eth0 inet static
	address 192.226.0.26
	netmask 255.255.255.252
	gateway 192.226.0.25
    
# ke Switch7
auto eth1
iface eth1 inet static
	address 192.226.0.129
	netmask 255.255.255.192
```

### Heiter
```
# ke Lawine
auto eth0
iface eth0 inet static
	address 192.226.0.130
	netmask 255.255.255.192
	gateway 192.226.0.129
    
# ke Switch8
auto eth1
iface eth1 inet static
	address 192.226.8.1
	netmask 255.255.252.0
```

## _Endpoint_
### RoyalCapital
```
auto eth0
iface eth0 inet static
	address 192.226.1.2
	netmask 255.255.255.0
	gateway 192.226.1.1
    up echo nameserver 192.168.122.1 > /etc/resolv.conf
```

### WilleRegion
```
auto eth0
iface eth0 inet static
	address 192.226.1.3
	netmask 255.255.255.0
	gateway 192.226.1.1
    up echo nameserver 192.168.122.1 > /etc/resolv.conf
```

### LakeKorridor
```
auto eth0
iface eth0 inet static
	address 192.226.0.66
	netmask 255.255.255.224
	gateway 192.226.0.65
    up echo nameserver 192.168.122.1 > /etc/resolv.conf
```

### LaubHills
```
auto eth0
iface eth0 inet static
	address 192.226.24.2
	netmask 255.255.248.0
	gateway 192.226.24.1
    up echo nameserver 192.168.122.1 > /etc/resolv.conf
```

### AppetitRegion
```
auto eth0
iface eth0 inet static
	address 192.226.24.3
	netmask 255.255.248.0
	gateway 192.226.24.1
    up echo nameserver 192.168.122.1 > /etc/resolv.conf
```

### RohrRoad
```
auto eth0
iface eth0 inet static
	address 192.226.16.2
	netmask 255.255.252.0
	gateway 192.226.16.1
    up echo nameserver 192.168.122.1 > /etc/resolv.conf
```

### SchwerMountains
```
auto eth0
iface eth0 inet static
	address 192.226.0.50
	netmask 255.255.255.248
	gateway 192.226.0.49
    up echo nameserver 192.168.122.1 > /etc/resolv.conf
```

### Richter
```
auto eth0
iface eth0 inet static
	address 192.226.0.42
	netmask 255.255.255.248
	gateway 192.226.0.41
    up echo nameserver 192.168.122.1 > /etc/resolv.conf
```

### Revolte
```
auto eth0
iface eth0 inet static
	address 192.226.0.43
	netmask 255.255.255.248
	gateway 192.226.0.41
    up echo nameserver 192.168.122.1 > /etc/resolv.conf
```

### Stark
```
auto eth0
iface eth0 inet static
	address 192.226.0.34
	netmask 255.255.255.252
	gateway 192.226.0.33
    up echo nameserver 192.168.122.1 > /etc/resolv.conf
```

### TurkRegion
```
auto eth0
iface eth0 inet static
	address 192.226.12.2
	netmask 255.255.255.0
	gateway 192.226.12.1
    up echo nameserver 192.168.122.1 > /etc/resolv.conf
```

### GrobeForest
```
auto eth0
iface eth0 inet static
	address 192.226.2.2
	netmask 255.255.255.0
	gateway 192.226.2.1
    up echo nameserver 192.168.122.1 > /etc/resolv.conf
```

### GranzChannel
```
auto eth0
iface eth0 inet static
	address 192.226.2.2
	netmask 255.255.254.0
	gateway 192.226.4.1
    up echo nameserver 192.168.122.1 > /etc/resolv.conf
```

### BredtRegion
```
auto eth0
iface eth0 inet static
	address 192.226.0.131
	netmask 255.255.255.192
	gateway 192.226.0.129
    up echo nameserver 192.168.122.1 > /etc/resolv.conf

auto br0
iface br0 inet static
    address 192.226.0.130
    netmask 255.255.255.192
    gateway 192.226.0.130
    up echo nameserver 192.168.122.1 > /etc/resolv.conf
    bridge_ports eth0
```

### RiegelCanyon
```
auto eth0
iface eth0 inet static
	address 192.226.8.2
	netmask 255.255.252.0
	gateway 192.226.8.1
    up echo nameserver 192.168.122.1 > /etc/resolv.conf
```

### Sein
```
auto eth0
iface eth0 inet static
	address 192.226.8.3
	netmask 255.255.252.0
	gateway 192.226.8.1
    up echo nameserver 192.168.122.1 > /etc/resolv.conf
```

## _Routing_
### Aura
```
# A1
route add -net 192.226.0.0 netmask 255.255.255.252 gw 192.226.0.1
# A2
route add -net 192.226.0.64 netmask 255.255.255.224 gw 192.226.0.1
# A3
route add -net 192.226.0.4 netmask 255.255.255.252 gw 192.226.0.1
# A4
route add -net 192.226.0.8 netmask 255.255.255.252 gw 192.226.0.1
# A5
route add -net 192.226.24.0 netmask 255.255.248.0 gw 192.226.0.1
# A6
route add -net 192.226.16.0 netmask 255.255.252.0 gw 192.226.0.1
# A7
route add -net 192.226.0.12 netmask 255.255.255.252 gw 192.226.0.1
# A8
route add -net 192.226.0.48 netmask 255.255.255.248 gw 192.226.0.1
# A9
route add -net 192.226.0.16 netmask 255.255.255.252 gw 192.226.0.17
# A10
route add -net 192.226.0.40 netmask 255.255.255.248 gw 192.226.0.17
# A11
route add -net 192.226.0.20 netmask 255.255.255.252 gw 192.226.0.17
# A12
route add -net 192.226.0.24 netmask 255.255.255.252 gw 192.226.0.17
# A13
route add -net 192.226.0.128 netmask 255.255.255.192 gw 192.226.0.17
# A14
route add -net 192.226.8.0 netmask 255.255.252.0 gw 192.226.0.17
# A15
route add -net 192.226.4.0 netmask 255.255.254.0 gw 192.226.0.17
# A16
route add -net 192.226.0.28 netmask 255.255.255.252 gw 192.226.0.17
# A17
route add -net 192.226.2.0 netmask 255.255.255.0 gw 192.226.0.17
# A18
route add -net 192.226.12.0 netmask 255.255.252.0 gw 192.226.0.17
# A19
route add -net 192.226.0.32 netmask 255.255.255.252 gw 192.226.0.17
# A20
route add -net 192.226.0.36 netmask 255.255.255.252 gw 192.226.0.37
# A21
route add -net 192.226.1.0 netmask 255.255.255.0 gw 192.226.0.37
```

### Denken
```
route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.226.0.37
```

### Frieren
```
route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.226.0.1

# A3
route add -net 192.226.0.4 netmask 255.255.255.252 gw 192.226.0.6
# A4
route add -net 192.226.0.8 netmask 255.255.255.252 gw 192.226.0.6
# A5
route add -net 192.226.24.0 netmask 255.255.248.0 gw 192.226.0.6
# A6
route add -net 192.226.16.0 netmask 255.255.252.0 gw 192.226.0.6
# A7
route add -net 192.226.0.12 netmask 255.255.255.252 gw 192.226.0.6
# A8
route add -net 192.226.0.48 netmask 255.255.255.248 gw 192.226.0.6
```

### Flamme
```
route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.226.0.5

# A4
route add -net 192.226.0.8 netmask 255.255.255.252 gw 192.226.0.9
# A5
route add -net 192.226.24.0 netmask 255.255.248.0 gw 192.226.0.9
# A7
route add -net 192.226.0.12 netmask 255.255.255.252 gw 192.226.0.13
# A8
route add -net 192.226.0.48 netmask 255.255.255.248 gw 192.226.0.13
```

### Fern
```
route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.226.0.9
```

### Himmel
```
route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.226.0.13
```

### Eisen
```
route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.226.0.17

# A16
route add -net 192.226.0.28 netmask 255.255.255.252 gw 192.226.0.29
# A17
route add -net 192.226.2.0 netmask 255.255.255.0 gw 192.226.0.29
# A18
route add -net 192.226.12.0 netmask 255.255.252.0 gw 192.226.0.29
# A11
route add -net 192.226.0.20 netmask 255.255.255.252 gw 192.226.0.21
# A12
route add -net 192.226.0.24 netmask 255.255.255.252 gw 192.226.0.21
# A15
route add -net 192.226.4.0 netmask 255.255.254.0 gw 192.226.0.21
# A13
route add -net 192.226.0.128 netmask 255.255.255.192 gw 192.226.0.21
# A14
route add -net 192.226.8.0 netmask 255.255.252.0 gw 192.226.0.21
```

### Lugner
```
route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.226.0.29
```

### Linie
```
route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.226.0.21

# A12
route add -net 192.226.0.24 netmask 255.255.255.252 gw 192.226.0.25
# A13
route add -net 192.226.0.128 netmask 255.255.255.192 gw 192.226.0.25
# A14
route add -net 192.226.8.0 netmask 255.255.252.0 gw 192.226.0.25
```

### Lawine
```
route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.226.0.25

# A13
route add -net 192.226.0.128 netmask 255.255.255.192 gw 192.226.0.129
# A14
route add -net 192.226.8.0 netmask 255.255.252.0 gw 192.226.0.129
```

### Heiter
```
route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.226.0.129
```

# Konfigurasi CIDR
![tree cidr](./F10_Tree-CIDR.jpg)