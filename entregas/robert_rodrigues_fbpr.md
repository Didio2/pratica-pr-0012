# Restauração Clonezilla Lite Server/Cliente

* **Robert Rodrigues Rosa Magalhães**
* **Tema:Backup e Restore**

## 1. Objetivo
O sistema de Backup e Restauração server para manter e preservar a integridade dos dados do cliente. Mantendo seguros mesmo após uma falha.

## 2. Ferramentas e Cuidados Técnicos
* **Ferramentas / Softwares:** clonezilla, gparted.
* **Segurança / Boas Práticas:** pulseira ESD, backup prévio, verificação de energia

## 3. Passo a Passo
1. Usando o Gparted Live faça o formate os 2 hds do Computador Servidor, usando a tabela de partição GPT, e formate em ext4. 

2. Usando o Clonezilla Live, no modo device-image, crie uma imagem do disco sda, e salve no disco sdb. 

- Deviceimage > localdev > CTRL_C > sdb1 > no-fsck > "TAB" > "Done" > Beginner > savedisk > Nomear Imagem > z9p > -sgoc > não copiar logs > choose. 

3. Após salvar Imagem do disco sda, use o Clonezilla live no modo Lite Server: 

- Lite-server > start > both > start-new-dhcpd( use esse modo caso não tenha uma rede DHCP ) > localdev > CTRL_C > sdb1 > no-fsck > "TAB" > "Done" > Beginner > massive-deployment > from-image > restoredisk > sda > -k0 > sim > choose > multicast > clients-to-wait > "coloque a quantidade de máquinas clientes" . 

4. Quando o servidor perguntar "Todos os clientes finalizarão as tarefas de restauração?" 
-  inicialize todas maquinas clientes usando Boot via rede.
-  Ao aparecer essa tela continue no modo multicast, deixe prosseguir

