# Elastic Defend + Proxmox.
![Slide 4_3 - 1](https://github.com/user-attachments/assets/80fa8efb-ba37-4d25-88ac-59c5944c54cf)
## Neste projeto demonstro como rodar a aplicação Elastic Defend, ferramenta de segurança que detecta, previne e responde a ameaças cibernéticas, esta aplicação assim como várias outras disponíveis no mercado fazem parte de um grupo de ferramentas chamado SIEM (Gerenciamento de Informações e Eventos de Segurança).

O Elastic Defend funciona basicamente "lendo" os logs, registros do sistema analisado (Linux, Windows e macOS), dados de rede (tráfego entre dispositivos), atividades endpoints (computadores, dispositivos móveis, etc) e Informações de aplicativos e serviços em nuvem. Em posse de todos os dados que pode reunir, o programa Indexa e Analisa todas as informações coletadas e é gerado o que se chama de Índice Invertido, este índice permite que as informações sejam rapidamente pesquisadas e analisadas, exemplo:  
Se um computador acessa um site malicioso, o Elastic Defend pode identificar essa atividade no índice e associá-la a um possível ataque.

Para isso, irei utilizar o Proxmox, uma plataforma de virtualização de código aberto que permite gerenciar máquinas virtuais (VMs) e contêineres, onde rodo minhas máquinas virtuais e onde 3 destas máquinas virtuais (2 Linux e 1 Windows) irão servir como "cobaias" para extrairmos dados e depois analisar.
