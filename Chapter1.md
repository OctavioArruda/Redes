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
