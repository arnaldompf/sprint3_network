# Projeto de Rede Corporativa para Laboratório Clínico

## Sobre o Projeto
Este projeto, desenvolvido no Cisco Packet Tracer, simula a infraestrutura de rede de um laboratório de análises clínicas. O objetivo foi criar uma rede segura, segmentada e escalável, projetada para ser a base de uma solução de gestão de estoque automatizada por Visão Computacional, resolvendo o "Desafio 1 - Baixa visibilidade no apontamento de consumo".

## Arquitetura
A arquitetura de rede segue o modelo **"Núcleo Colapsado" (Collapsed Core)** e é composta pelos seguintes componentes:

- **Roteador Central**: Responsável pelo roteamento Inter-VLAN ("Router on a Stick"), permitindo a comunicação controlada entre os diferentes setores.
- **Switch de Distribuição (Core)**: Agrega o tráfego de todos os switches de acesso, otimizando o fluxo de dados e a escalabilidade.
- **Switches de Acesso**: Conectam os dispositivos finais e aplicam a segmentação lógica através de VLANs.
- **Segmentação Lógica (VLANs)**:
  - **VLAN 10 (`VLAN_SERVIDORES`):** Isola a infraestrutura crítica.
  - **VLAN 20 (`VLAN_ANALISES`):** Rede para os computadores do setor técnico.
  - **VLAN 30 (`VLAN_RECEPCAO`):** Rede para o setor administrativo.
  - **VLAN 40 (`VLAN_Gerencia`):** Rede Wi-Fi para mobilidade da equipe de gestão.

## Tecnologias Utilizadas
- **VLANs (IEEE 802.1Q)**: Para a segmentação lógica da rede.
- **Roteamento Inter-VLAN**: Para a comunicação entre as VLANs.
- **Subnetting IPv4 (CIDR)**: Para o planejamento e otimização do endereçamento IP.
- **Trunking (IEEE 802.1Q)**: Para permitir o tráfego de múltiplas VLANs em um único link.
- **Endereçamento Estático**: Para garantir o controle dos endereços na rede.

## Requisitos
- **Hardware (Simulado)**:
  - 1x Roteador (Modelo 1941)
  - 5x Switches (Modelo 2960)
  - 1x Servidor
  - 6x Computadores (Hosts)
  - 1x Access Point
  - 1x Notebook
- **Software**:
  - Cisco Packet Tracer (Versão 8.0 ou superior)

## Instruções de Uso
1. Abra o arquivo `.pkt` do projeto no Cisco Packet Tracer.
2. Aguarde alguns segundos para a convergência completa da rede (todas as luzes de link devem ficar verdes).
3. Para validar, realize testes de `ping` entre computadores de VLANs diferentes (ex: `ping 192.168.50.10` a partir de um PC da VLAN 20).
4. Acesse o Web Browser de qualquer PC e navegue para `http://192.168.50.10` para confirmar o acesso ao serviço do servidor.

## Integrantes 

- Arnaldo Filho -    RM 555780
- Erick Fujita -     RM 556096
- Fabrício Carlos -  RM 555017
- João Boht -        RM558690
