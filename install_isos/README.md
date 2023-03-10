# Alguns Nodes 🖥️💻🎛️
aqui você pode extrair algumas formas e diretas de adicionar alguns nodes importantes para o seu laboratório.

### node Linux CentOS 7
crie o diretrio neste caminho
`cd /opt/unetlab/addons/qemu && mkdir linux-centos-7 && cd linux-centos-7`

baixe a imagem dentro do diretório
`wget http://mirror.ufam.edu.br/centos/7.9.2009/isos/x86_64/CentOS-7-x86_64-Minimal-2207-02.iso`

renomeie ela configure ela para o ambiente
```sh
mv CentOS-7-x86_64-Minimal-2207-02.iso cdrom.iso
/opt/qemu/bin/qemu-img create -f qcow2 virtioa.qcow2 30G
```

### node Switch Cisco IOL
link switch Cisco IOL, baixe tudo zipado
https://drive.google.com/drive/folders/18jDCPBz8JYcOguH1nz6YMR-9Qt4BUN54

mova o zip para esse diretorio
`mv aquivo.zip /opt/unetlab/addons/iol/bin`

descompacte e suba tudo para a pasta bin
`unzip arquivo.zip && mv arquivo/* .`

rode o unl_wrapper
`/opt/unetlab/wrappers/unl_wrapper -a fixpermissions`

### node mikrotik Router OS
crie um diretório
`mkdir /opt/unetlab/addons/qemu/mikrotik-6.48.6`

navegue até o mesmo
`cd /opt/unetlab/addons/qemu/mikrotik-6.48.6`

baixe a imagem
`wget https://download.mikrotik.com/routeros/6.48.6/chr-6.48.6.img.zip`

descompacte o arquivo baixado
`unzip chr-6.48.6.img.zip`

renomeie a imagem para que o eve possa trabalhar
`mv chr-6.48.6.img hda.qcow2`

remova o restante
`rm chr-6.48.6.img.zip`

 ode o unl_wrapper
`/opt/unetlab/wrappers/unl_wrapper -a fixpermissions`


### node AlienVault Cybersecurity OSSIM
```
mkdir /opt/unetlab/addons/qemu/alienvault-ossim-5.8.5

cd /opt/unetlab/addons/qemu/alienvault-ossim-5.8.5

wget https://cdn-cybersecurity.att.com/downloads/AlienVault_OSSIM_64bits.iso

mv AlienVault_OSSIM_64bits.iso cdrom.iso

/opt/qemu/bin/qemu-img create -f qcow2 hda.qcow2 50Gkkk
```

### node zabbix
```
mkdir /opt/unetlab/addons/qemu/zabbix-6.2.7/

cd /opt/unetlab/addons/qemu/zabbix-6.2.7/

wget https://cdn.zabbix.com/zabbix/appliances/stable/6.2/6.2.7/zabbix_appliance-6.2.7-qcow2.tar.gz

tar xzf zabbix_appliance-6.2.7-qcow2.tar.gz

rm zabbix_appliance-6.2.7-qcow2.tar.gz

cd zabbix_appliance-6.2.7-qcow2

mv zabbix_appliance-6.2.7.qcow2 /opt/unetlab/addons/qemu/zabbix-6.2.7/virtioa.qcow2

rm -rf zabbix_appliance-6.2.7-qcow2/

/opt/unetlab/wrappers/unl_wrapper -a fixpermissions
```




<!--

# Adicione uma network cloud0

# Adicione dois routers e os conecte a rede network criada

# Adicione um switch e conecte aos routers

# Adicione um Virtual PC e o conect ao switch
-->


