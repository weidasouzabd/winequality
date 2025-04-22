# winequality
Projeto II - Aplicação de Métodos de Aprendizagem de Máquina
Análise Preditiva da Qualidade de Vinhos: Uma Abordagem com Machine Learning
Este projeto apresenta uma análise abrangente e desenvolvimento de um sistema inteligente para avaliação e predição da qualidade de vinhos, utilizando técnicas avançadas de Machine Learning. O estudo combina diferentes abordagens de aprendizado de máquina para criar um sistema robusto de classificação e análise de vinhos, baseado em suas características físico-químicas.

Objetivo
O objetivo principal é desenvolver um modelo preditivo capaz de:

Classificar vinhos quanto à sua qualidade
Identificar padrões e características determinantes
Prever a probabilidade de um vinho ser premiado
Fornecer recomendações baseadas em dados
A qualidade do vinho envolve relações complexas entre as variáveis

Temos um número razoável de features (11)
O problema é de classificação binária
Precisamos de boa generalização para novos vinhos
Especificação Técnica
Dataset: Para desenvolvimento desse projeto, será utilizado dataset específico baixado no site Kagle. Este data set é formado por características quimicas de vinhos tintos, dando a eles uma pontuação de acordo com essas características. A base de dados se encontra em meu google drive no endereço: '/content/drive/MyDrive/winequality-red.csv'

Formato: A base de dados está em formato CSV, estando divivido em 12 colunas (features) conforme segue: Acidez Fixa, Acidez Volátil, Acido Citrico, Açucar Residual, Cloreto, Dioxido de Enxofre Livre, Dioxido de Enxofre Total, Densidade, pH, Sulfato, Alcool e Qualidade.

Separando Target (Objetivo):

y = data['Qualidade'] Separa a coluna de qualidade Criando Classificação Binária:Como classificar vinhos em "premium" (≥7) e "padrão" (<7) Foram Transformados notas em "sim" (1) ou "não" (0)

Dividindo os Dados:

-Treino: Vinhos para o sistema aprender (80%)

-Teste: Vinhos para verificar o aprendizado (20%)

Pré processamento Por que cada etapa é importante?

Limpeza: . Remove erros . Padroniza formatos . Trata valores problemáticos
Normalização: . Coloca tudo na mesma escala . Melhora o aprendizado . Evita problemas com números muito diferentes
Classificação Binária: . Simplifica o problema . Torna a decisão mais clara . Facilita a avaliação
Divisão dos Dados: . Permite testar o aprendizado . Evita "colar" no teste . Valida o modelo
Resultado Final: Dados limpos, organizados e prontos para uma analise efetiva e relevante.

É como ter uma cozinha organizada onde: • Ingredientes estão limpos • Medidas estão padronizadas • Tudo está separado e pronto para usar Esta etapa é fundamental porque: • Dados limpos = Melhores resultados • Dados padronizados = Aprendizado mais eficiente • Dados bem organizados = Análise mais confiável

Métodos de Pré-processamento: Passos

Limpar adequadamente os dados numéricos
Converter strings para números float
Tratar valores ausentes (caso haja)
Realizar a normalização
DESCRIÇÃO DAS FEATURES: Acidez Fixa: float Acidez Volátil: float Acido Citrico: float Açucar Residual: float Cloreto: float Dioxido de Enxofre Livre: float Dioxido de Enxofre Total: float Densidade: float pH: float Sulfato: float Alcool: float Qualidade: numerico

**Tarefa de Aprendizado:

Redes Neurais Artificiais:

Usa TensorFlow para criar uma rede neural profunda
Inclui camadas de dropout para evitar overfitting
Monitora a acurácia durante o treinamento
Algoritmos de Agrupamento:

Implementa K-means
Determina automaticamente o melhor número de clusters
Visualiza a distribuição dos clusters
Algoritmos de Associação:

Usa o algoritmo Apriori
Descobre padrões frequentes nos dados
Gera regras de associação
Processamento de Linguagem Natural:

Cria descrições textuais dos vinhos
Aplica vetorização TF-IDF
Analisa padrões textuais
Sistema de Previsão:

Interface interativa para novos vinhos
Combina resultados de diferentes modelos
Fornece análise completa
Modos de aprendizado: Supervisionado.

Algoritmos Avaliados: Redes Neurais Artificiais, Algoritmos de Agrupamento K-means, Algoritmos de Associação, Processamento de Linguagem Natural.

Métrica utilizadas:

Acurácia (Accuracy):
Mede a proporção de previsões corretas Fórmula: (Verdadeiros Positivos + Verdadeiros Negativos) / Total Exemplo: Se acurácia = 0.85, 85% das previsões estão corretas

Binary Crossentropy (Perda):

Mede o erro nas previsões probabilísticas Quanto menor, melhor Útil para classificação binária (premiado/não premiado)

Para o K-means (Clustering): Silhouette Score: Mede a qualidade dos clusters Varia de -1 a 1
1: Clusters bem definidos 0: Clusters sobrepostos -1: Clusters incorretos

Ajuda a escolher o número ideal de clusters

Para as Regras de Associação: Métricas principais:
Suporte (Support):

Frequência do padrão nos dados Exemplo: Suporte = 0.1 significa que o padrão aparece em 10% dos casos

Confiança (Confidence):

Probabilidade condicional da regra Exemplo: Confiança = 0.8 significa que a regra é verdadeira em 80% dos casos

Lift:

Mede a força da associação Lift > 1: Associação positiva Lift = 1: Sem associação Lift < 1: Associação negativa

Métricas de Classificação Detalhadas: Este relatório inclui:
Precisão (Precision):

Dos vinhos previstos como premiados, quantos realmente são Fórmula: VP / (VP + FP) Importante para minimizar falsos positivos

Recall (Sensibilidade):

Dos vinhos realmente premiados, quantos foram identificados Fórmula: VP / (VP + FN) Importante para não perder vinhos bons

F1-Score:

Média harmônica entre precisão e recall Equilibra falsos positivos e falsos negativos Bom para datasets desbalanceados

Matriz de Confusão (implícita no relatório):

Verdadeiros Positivos (VP) Falsos Positivos (FP) Verdadeiros Negativos (VN) Falsos Negativos (FN)

Visualizações de Performance: O que mostra:

Curva de Aprendizado:

Como a acurácia melhora com o tempo Identifica overfitting/underfitting Valida a estabilidade do modelo

Validação Cruzada (implícita):

Usa 20% dos dados para validação Evita overfitting Verifica generalização

Estas métricas em conjunto fornecem uma visão completa do desempenho do sistema, permitindo: Avaliar qualidade Identificar problemas Guiar melhorias Validar resultados
