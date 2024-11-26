# Elastic Defend + Proxmox.
![Slide 4_3 - 1](https://github.com/user-attachments/assets/80fa8efb-ba37-4d25-88ac-59c5944c54cf)
## Demonstro aqui como rodar a aplicação Elastic Defend, ferramenta de segurança que detecta, previne e responde a ameaças cibernéticas, esta aplicação assim como várias outras disponíveis no mercado fazem parte de um grupo de ferramentas chamado SIEM (Gerenciamento de Informações e Eventos de Segurança).

Estas aplicações funcionam basicamente "lendo" os logs, registros do sistema analisado (Linux, Windows e macOS), dados de rede (tráfego entre dispositivos), atividades endpoints (computadores, dispositivos móveis, etc) e Informações de aplicativos e serviços em nuvem. Com esses dados reunidos, o programa Indexa e Analisa todas as informações coletadas e é gerado o que se chama de Índice Invertido, este índice permite que as informações sejam rapidamente pesquisadas e analisadas, exemplo:  

- _Se um computador acessa um site malicioso, o Elastic Defend pode identificar essa atividade no índice e associá-la a um possível ataque._

Para isso, irei utilizar o Proxmox, plataforma de virtualização _open source_ que permite gerenciar máquinas virtuais (VMs) e contêineres, nesse exmplo utilizo 3 destas máquinas virtuais (2 Linux e 1 Windows) que irão servir como base para extrairmos dados e depois analisar.

> Neste documento irei focar na demonstração do processo de recolhimento de informações das VMs, posteriormente irei criar um tutorial básico de como implementar tanto o Elastic Defend quanto o Proxmox.

## 1. Passo - Inicializar as máquinas virtuais:
![VMs](https://github.com/user-attachments/assets/10129944-abc9-4e44-8a0e-b0cf1fbcbae9)

