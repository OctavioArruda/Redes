# 1.4 Atraso, perda, throughput em redes(network)

## Como perda e atrasos ocorrem?

- Pacotes ficam bufferizados nos buffers dos roteadores
- Taxa de chegada de pacotes sobrepõe taxa de saída do link
- Pacotes esperam por seu turno

- Atraso de processamento nodal:
	- Depende de várias variáveis
		- Tam. pacote, tam. tabela encaminhamento
	- Tipicamente variável, grandeza msec 
- Atraso de enfileiramento:
	- Tempo que o pacote espera no link(fila) de saída para ser transmitido
	- Altamente variável
	- Depende do estado de congestionamento do roteador
- Atraso de transmissão:
	- Tempo para colocar os bits no barramento
	- 1 byte = 8 bits...1024 bytes = 8192 bits
	- Tam. do pacote em bits / largura de banda
	- Atraso variável, depende dos bits
- Atraso de propagação:
	- d: tamanho do link físico
	- s: velocidade de propagação(~2x10^8 m/sec)
	- dprop = d/s

- Notas extras sobre delay de enfileiramente(queueing delay):
	- Seja R a largura da banda(link bandwidth)
	- Seja L o tamanho do pacote(packet length)
	- a: taxa de chegada de pacotes
		- L*a/R ~ 0 queueing delay very small
		- L*a/R -> 1: avg. queueing delay is large
		- L*a/R > 1: chega mais pacotes do que podem ser tratados, delay médio tende ao infinito
	
- Calculando delay:
	- *traceroute* program: calcula delay enviando pacotes da origem para o destino, variando o ttl(time to leave)
	- Para cada router, o ttl é zerado, para que o pacote expire, e seja possível saber o tempo até cada router
	- O ping que o traceroute mostra é uma média de todas as rotas encontradas até o end host

- Perda acontece quando o buffer de um link, router ficar completamente cheia
- Pacote perdido pode ser retransmitido pelo nodo anterior, origem ou nem ser retransmitido

- Throughput
- taxa na qual os bits são transferidos entre origem e destino

## 1.5 Protocol layers, service models
- Protocol "layers" - camadas de protocolo
- network complexa, dividida em várias partes

- Como conseguimos organizar o ecossistema da network para funcionar bem? Divisão em camadas
- Diminuir a complexidade de algo equivale a modularizar
- Complexidade de redes organizada em camadas na mesma premissa do desenvolvimento de software
- Camadas:
	- application: A camada de aplicação é a camada em que nós vamos implementar os protocolos de camada de comunicação(http, ftp(file transfer protocol p arquivos), smtp(emails), por ex)
	- transport: camada de transporte, responsável por transportar os pacotes que saiam da máquina origem e chegam na máquina destino. Esta camada faz o trabalho de permitir que os processos de software da máquina origem consigam endereçar os processos de software da máquina destino.
	- network: camada que uniformiza tudo. Permite que os pacotes de rede saiam da rede da origem, sendo encaminhandos roteador a roteador até chegar no destino. Responsável por fazer roteamento
	- link(enlace): transferência de bloco de dados entre um elemento de rede e seu vizinho
	- physical: transferência de bits

- Somente a camada de rede, de transporte e de aplicação é padronizada na internet

- ISO/OSI reference model
	- Camada de apresentação: Enviar dados com anotação que identifica qual é a função, ou como é montado. Desta forma, como chega no end host, pode ser melhor interpretado.
	- Camada de sessão: Ao transferir um arquivo no FTP, ao dar um problema na rede, perde-se tudo. É necessário começar tudo de novo. A ideia da camada de sessão é lidar com isso.
	
- Cada camada adiciona um cabeçalho da sua camada, com informações necessárias para poder executar as funções que se espera dessa camada.

## 1.6 Networks under attack: security

- Segurança em redes
- Não faz parte do escopo da disciplina detalhar muito sobre segurança em redes
- De fato a internet não foi desenhada com segurança em mente
- A internet nasceu na forma de uma iniciativa entre um conjunto de usuários localizados entre universidades que queriam trocar dados
- Usuários mutuamente confiáveis, sem razão para pensar em protocolos de segurança
- Segurança semre foi um "remendo"
- Proliferação de malwares:
  - Hosts finais acabam recebendo objetos maliciosos que são acionados pelos usuários ou são executados mesmo que o usuário não peça para executar.
  - Definição de vírus ou worm
  - worm: instância sofisticada em que o usuário não precisa pedir para executar
  - Ponto de partida para a construção de botnet: máquinas zombies que normalmente nem sabem que estão infectadas e podem iniciar um ataque contra um serviço
  - Ip spoofing: envia pacotes com falsos endereços de origem

## 1.7 History of internet
- Professor disse para ler no livro, não comentou nada
	
	
	
	
	
	
	
	
	
	
	
	
	
	
	
	
	
	
