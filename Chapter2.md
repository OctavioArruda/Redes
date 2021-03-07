# Chapter 2 - Application Layer (Camada de aplicação)

## Aspectos conceituais

## 2.1 Princípios de aplicações de network 
- Algumas aplicações de internet:
  - email
  - web
  - text messaging
  - remote login
  - multi-user network games
- Formas de estruturar aplicações:
  - Client-server
  - peer-to-peer (P2P)
- Arquitetura cliente-servidor
    - Servidor: 
      - Sempre no host
      - IP estático
      - data centers para escalar
    - Cliente:
      - Comunica-se com o servidor
      - Pode estar conectado ou não, intermitentemente
      - Pode ter ip dinâmico
      - Não se comunicam entre si
- Arquitetura P2P 
  - Não temos um servidor sempre disponível(embora não seja totalmente verdade)
  - Normalmente tem algum tipo de servidor, mas não se presta a atender a requisição, acaba sendo um ponto de encontro para se encontrar com outro usuário
-  Na arquitetura cliente-servidor, os clientes não se comunicam diretamente entre si
-  Na arquitetura cliente-servidor, o servidor possuí um endereço fixo e bem conhecido, e em razão do servidor estar sempre online, um cliente sempre consegue se conectar enviando um pacote para o endereço de ip do servidor.
-  Exemplos de aplicações cliente-servidor: Web, FTP, Telnet, e-mail
-  Um server host pode ser insuficiente, muitas requisições podem travar o servidor
   -  Por este motivo, usa-se **data centers**, uma casa com vários hosts, utilizados para criar um serviço virtual poderoso
   -  Um data center pode ter centenas de milhares servidores
- Na arquitetura peer 2 peer não há grandes necessidades de servidores dedicados em data-centers