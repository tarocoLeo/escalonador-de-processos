# Escalonador de Processos
#### Trabalho: Sistemas Operacionais

O projeto deverá implementar um algoritmo para escalonar processos. Para isto teremos como dados de entrada: ID do processo, Hora de entrada (pegar do sistema), tempo de execução (frações de segundos) do processo e time slice (fatia do tempo de uso do processador, tb em frações de segundos). Cada processo poderá ter ainda como dado de entrada a prioridade (por definição 1 para todos) e, caso algum tenha a necessidade de ser prioritário na execução este valor deverá ser maio que 1. O processo de maior prioridade deverá ser executado.

A cada iteração... mostrar a fila dos processos prontos... bem como quem está na execução e, possíveis processos já finalizados. Caso algum tenha prioridade... fazer o decremento dela a cada execução para que não haja monopólio em sua execução...

#####Veja uma simulação:

Process ID | Tempo Entrada | Tempo de Execução | Prioridade
:---------:|:-------------:|:-----------------:|:---------:
1 | 15:30 | 30 | 1
2 | 15:33 | 20 | 1
3 | 15:40 | 25 | 1
4 | 15:42 | 15 | 2


Time slice: 5 CPU [ ]

---
A fila de processos deverá ser criada primeiramente, respeitando da maior para a menor prioridade... caso dois ou mais processos tenham a mesma prioridade, deverá ser considerado o primeiro que chegou (menor hora de entrada).

Uma vez que a fila esteja pronta... o escalonador deverá proceder com as execuções do processor e, respeitar a fila, pois caso ainda não tenha terminado, ele deverá voltar para a fila com novos dados de entrada (nova hora de entrada e tempo restante de execução para seu término)

Faça as impressões das etapas para que se possa acompanhar o escalonador...

Permitir que a cada momento, novos processos possam ser inseridos na fila de processos prontos.