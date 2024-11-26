# Elastic Defend + Proxmox.
![Slide 4_3 - 1](https://github.com/user-attachments/assets/80fa8efb-ba37-4d25-88ac-59c5944c54cf)
## Demonstro aqui como rodar a aplicação Elastic Defend, ferramenta de segurança que detecta, previne e responde a ameaças cibernéticas, esta aplicação assim como várias outras disponíveis no mercado fazem parte de um grupo de ferramentas chamado SIEM (Security Information and Event Management - Gerenciamento de Informações e Eventos de Segurança).

Estas aplicações funcionam basicamente "lendo" os logs, registros do sistema analisado (Linux, Windows e macOS), dados de rede (tráfego entre dispositivos), atividades endpoints (computadores, dispositivos móveis, etc) e Informações de aplicativos e serviços em nuvem. Com esses dados reunidos, o programa Indexa e Analisa todas as informações coletadas e é gerado o que se chama de Índice Invertido, este índice permite que as informações sejam rapidamente pesquisadas e analisadas, exemplo:  

- _Se um computador acessa um site malicioso, o Elastic Defend pode identificar essa atividade no índice e associá-la a um possível ataque._

Para isso, irei utilizar o Proxmox, plataforma de virtualização _open source_ que permite gerenciar máquinas virtuais (VMs) e contêineres, nesse exmplo utilizo 3 destas máquinas virtuais (2 Linux e 1 Windows) que irão servir como base para extrairmos dados e depois analisar.

> Neste documento irei focar na demonstração do processo de recolhimento de informações das VMs, posteriormente irei criar um tutorial básico de como implementar tanto o Elastic Defend quanto o Proxmox.

## 1. Inicializar as máquinas virtuais:
Com as máquinas em execução e após as configurações iniciais (criação de uma conta no portal do Elastic Cloud, instalação e configuração do agente Elastic Defend) podemos iniciar os trabalhos de verificação dos relatórios emitidos pela ferramenta, neste exemplo irei tanto apresentar alguns registros comuns de funcionamento quanto após a instalação e execução de algumas aplicações nos ambientes virtualizados.

![VMs](https://github.com/user-attachments/assets/10129944-abc9-4e44-8a0e-b0cf1fbcbae9)

## 2. Logar no portal do Elastic Cloud:
Após a criação de uma conta no portal do Elastic Cloud, verá algo como:

![image](https://github.com/user-attachments/assets/875882fb-dda8-4fda-a5af-bb829e755e8f)

O Elastic Cloud possui um período de testes gratuito, para o nosso propósito vai servir tranquilamente.
Após logar no portal da aplicação, vemos no primeiro campo os ambientes que configuramos:

![image](https://github.com/user-attachments/assets/175627bd-6539-4a24-937f-e3dbb02f4292)

## 3. Gerar eventos de segurança para serem capturados pelo Elastic Defend:
![image](https://github.com/user-attachments/assets/ec71e64a-adaa-4343-92db-369a2dbd9048)

Neste exemplo estou executando a aplicação **NMAP** e rodando uma varredura de portas e outros tipos em outra das máquinas virtuais (linux lite), na imagem podemos ver o comando sendo executado e o que foi encontrado, em seguida iremos visualizar no dashboard/painel do Elastic Cloud.
