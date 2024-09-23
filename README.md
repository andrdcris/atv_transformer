# Transformer Translation Model: Portuguese to English]

Este repositório contém um [tutorial](https://colab.research.google.com/drive/1NJUDn7gI9LaFrYYSfAbHaAN1OJ_P7sfE?usp=sharing&authuser=7#scrollTo=4UwEMtts1LVA&uniqifier=22) para treinar um modelo Transformer com o objetivo de traduzir frases do português para o inglês. O modelo baseia-se no conceito de autoatenção, possibilitando que ele processe entradas de tamanho variável e capture dependências de longo alcance em sequências de texto. Abaixo estão descritos os principais pontos positivos e negativos percebidos na implementação.

## Pontos Positivos
1. O modelo Transformer utiliza autoatenção, permitindo capturar dependências distantes entre as palavras, o que é especialmente útil para traduções onde o significado de uma palavra pode ser influenciado por palavras distantes na frase.

2. Diferentemente de RNNs, o Transformer permite que as saídas de cada camada sejam calculadas em paralelo, aumentando significativamente a eficiência durante o treinamento, especialmente em grandes conjuntos de dados.

## Pontos Negativos
1. Ineficiência para Séries Temporais: Para tarefas com relação temporal ou de séries temporais, como na tradução de frases em que a ordem das palavras é importante, a saída para cada passo de tempo é calculada usando todo o histórico. Isso pode ser menos eficiente do que abordagens que se baseiam apenas no estado atual e nas entradas passadas.

2. Necessidade de Codificação Posicional: Quando o modelo é aplicado a dados com relações temporais ou espaciais, como no texto, é necessário adicionar codificação posicional, uma vez que o Transformer, por padrão, trata as entradas como um pacote de palavras sem ordem intrínseca.

3. Requisitos Computacionais Elevados: Devido à sua arquitetura paralela e à necessidade de processar o contexto completo de uma sequência, o Transformer geralmente requer mais recursos computacionais, tanto em termos de memória quanto de poder de processamento, em comparação com modelos baseados em RNN ou CNN.

4. Complexidade de Implementação: Embora o Transformer ofereça muitas vantagens, sua implementação é mais complexa do que RNNs ou CNNs tradicionais, exigindo um conhecimento sólido de conceitos como autoatenção, atenção multi-cabeças e codificação posicional.

## Testes
Pricipais resultados: 
