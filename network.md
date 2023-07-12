- Add an interface:
  - ip link add dummy0 type dummy
  - ip link set dummy0 up
  - ip addr add 169.254.255.254/31 dev dummy0
  - ip route add default via 169.254.255.255 dev dummy0 metric 1000
  
