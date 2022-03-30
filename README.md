# Analise de sentimentos de tweets
----------------
## Introdução

Nesse décimo projeto o foco será utilizar técnicas de processamento de linguagem natural (NLP). Utilizaremos um Dataset obtido do Twitter com 100K postagens entre os dias 01/08/2018 e 20/10/2018. Cada postagem é classificada como positiva, negativa ou neutra.

Descrição das colunas:
- id: ID único para o tweet
- tweet_text: Texto da publicação no Twitter
- tweet_date: Data da publicação no Twitter
- sentiment: 0, se negativo; 1, se positivo; 2, se neutro
- query_used: Filtro utilizado para buscar a publicação

O objetivo do projeto será desenvolver um modelo para detectar o sentimento de uma publicação do Twitter a classificando em uma das três categorias: positiva, negativa ou neutra. O texto da publicação está disponível na coluna "tweet_text". 

## Etapas

O projeto consistirá em 3 etapas:

- 1) Análise da consistência dos dados
- 2) Análise exploratória e Pré-processamento
- 3) Modelagem e conclusões

## Conclusões e resultados alcançados

 sentiment| precision  |  recall  |f1-score  | support
 ---------|--------|-----------|----------|-------------
 0  | 0.75 |  0.72 |   0.74    |  9559
 1  | 0.70 |  0.72   |   0.71    |  9555
 2  | 0.92 |  0.94   |   0.93    |  9386
 ---------|--------|-----------|----------|-------------
 accuracy    |   |    |          |      0.79  |   28500
   macro avg    |   0.79   |   0.79  |    0.79    | 28500
weighted avg    |   0.79   |   0.79   |   0.79   |  28500

No final nosso modelo ficou muito bom em acertar sentimentos neutros e relativamente bom em identificar sentimentos negativos. Já em relação aos sentimentos positivos ele fico um pouco melhor do que a média.

Considerando que poderíamos usar modelos como esses para classificar os tweets e, por exemplo, evitar o churn de usuários/clientes nosso modelo seria eficiente em 75% dos casos, o que já seria bem interessante considerando o potencial de redução de churn. Em relação aos sentimentos neutros o modelo poderia ser usado como um termômetro para comunicações da empresa com seus clientes para medir se houve ou não reação a aquele tipo de comunicação/mensagem aos clientes.

Seria possível usar um modelo de stacking em que criaríamos modelos especialistas para cada tipo de sentimento ou tentar usar redes neurais profundas buscando aumentar a qualidade das métricas. Esses dois testes ficarão como desenvolvimentos futuros para esse projeto
