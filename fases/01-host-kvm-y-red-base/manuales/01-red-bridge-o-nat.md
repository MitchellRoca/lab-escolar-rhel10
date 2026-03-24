# Configuración de la Red Virtual 'colegio-net'

Para que las 4 máquinas virtuales se comuniquen, definimos este archivo XML:

```xml
<network>
  <name>colegio-net</name>
  <forward mode='nat'/>
  <bridge name='virbr-colegio' stp='on' delay='0'/>
  <ip address='192.168.100.1' netmask='255.255.255.0'>
    <dhcp>
      <range start='192.168.100.100' end='192.168.100.150'/>
    </dhcp>
  </ip>
</network>
