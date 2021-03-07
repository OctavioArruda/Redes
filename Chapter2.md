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
  - Normalmente tem algum tipo de servidor, mas não se presta a atender a requisição, acaba sendo um ponto de encontro para se encontrar com outro usuários