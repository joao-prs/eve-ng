# legendas
clique em botao >
edite um campo  -



# passo a passo do router
Interfaces(janela)
  > VRRP(aba) > add(+)
    > Interfaces(janela) > VRRP(aba)
      - Interface: ether2-switch
      - VRID: 20
      - Priority: 150
      - Interval: 1.00
      - Preemption Mode: [x]
      - Authentication: none

IP Addresses(janela)
  > add(+)
    - Address: 192.168.1.1/24        # ip do router para o switch
    - Interface: ether1-link
  > add(+)
    - Address: 192.168.1.254/32
    - Interface: vrrp1

IP Firewall(janela)
  > NAT(aba) > add(+)
    > General(aba)
      - Out. Interface: ether1-link
    > Action(aba)
      - Action: masquerade





# configure o ip do PC
VPC> ip 192.168.1.10/24 192.168.1.254
