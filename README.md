# Trabalho de IA — Controle de Elevadores com Aprendizado por Reforço

## Integrantes
- Eduarda Paulino
- Lavínia Oliveira

---

## Problema

Desenvolver um sistema de controle de elevadores utilizando **Aprendizado por Reforço (Reinforcement Learning — RL)**, com o objetivo de determinar uma estratégia eficiente para coordenar dois elevadores em um prédio de 10 andares, reduzindo o tempo médio de espera dos passageiros.

O agente interage com o ambiente, observa o estado dos elevadores e as chamadas dos passageiros, escolhe ações e recebe recompensas de acordo com os resultados obtidos. Por meio de tentativa e erro, ele aprende uma política que busca maximizar a recompensa acumulada ao longo do tempo.

## Modelagem do problema como MDP

O problema é representado como um **Processo de Decisão de Markov (MDP)**, composto por três elementos principais:

- **Estado:** posição e direção dos elevadores, estado das portas, chamadas dos andares, destinos selecionados nas cabines e quantidade de passageiros transportados.
- **Ações:** subir, descer, abrir a porta ou esperar. Como cada elevador possui quatro ações possíveis, existem 16 combinações de ações conjuntas para os dois elevadores.
- **Recompensas:** valores que orientam o aprendizado do agente, incentivando o atendimento rápido dos passageiros e penalizando esperas prolongadas, movimentos desnecessários e abertura de portas sem passageiros.

## Objetivo

Aprender uma política de controle capaz de coordenar os elevadores de maneira eficiente, considerando as chamadas dos passageiros e as condições atuais do ambiente. O desempenho do agente poderá ser avaliado pelo tempo médio de espera e comparado com uma estratégia de referência baseada em regras fixas.
