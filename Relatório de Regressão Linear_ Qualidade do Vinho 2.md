# Relatório de Regressão Linear: Qualidade do Vinho

**Autor:** Gabriel Braga Ledo Luduvico
**RA:** 22404076





## Introdução

Este relatório apresenta os resultados de uma análise de regressão linear realizada no conjunto de dados "Wine Quality" do UCI Machine Learning Repository. O objetivo foi modelar a qualidade do vinho (variável de saída) com base em suas características físico-químicas (variáveis de entrada).

## Metodologia

O conjunto de dados "Wine Quality" (ID 186) foi obtido do UCI Machine Learning Repository. Ele contém 6497 instâncias e 11 características físico-químicas, além da variável de qualidade. O dataset foi dividido em conjuntos de treino e teste (80% treino, 20% teste). Um modelo de regressão linear foi treinado usando o conjunto de treino e avaliado no conjunto de teste.

## Resultados

### Métricas de Avaliação

Após o treinamento e a avaliação do modelo, as seguintes métricas foram obtidas:

- **Erro Quadrático Médio (MSE):** 0.5467

- **Coeficiente de Determinação (R2):** 0.2598

O valor de R2 indica que aproximadamente 26% da variância na qualidade do vinho pode ser explicada pelas características físico-químicas incluídas no modelo. O MSE representa a média dos quadrados dos erros, ou seja, a diferença quadrática média entre os valores previstos e os valores reais.

### Coeficientes do Modelo

Os coeficientes do modelo de regressão linear indicam a influência de cada característica físico-química na qualidade do vinho. Um coeficiente positivo sugere que um aumento na característica está associado a um aumento na qualidade, enquanto um coeficiente negativo sugere o oposto.

| Característica | Coeficiente |
| --- | --- |
| sulphates | 0.8084 |
| pH | 0.4828 |
| alcohol | 0.2707 |
| fixed_acidity | 0.0790 |
| residual_sugar | 0.0459 |
| free_sulfur_dioxide | 0.0070 |
| total_sulfur_dioxide | -0.0027 |
| citric_acid | -0.1438 |
| chlorides | -0.3328 |
| volatile_acidity | -1.3508 |
| density | -58.9451 |

É importante notar que a `density` e a `volatile_acidity` possuem os maiores coeficientes em magnitude, indicando uma forte relação (negativa) com a qualidade do vinho.

### Visualizações

#### Matriz de Correlação

A matriz de correlação abaixo ilustra as relações entre todas as variáveis do dataset. Cores mais quentes indicam correlação positiva, enquanto cores mais frias indicam correlação negativa.

![Matriz de Correlação](https://private-us-east-1.manuscdn.com/sessionFile/K1mQJZl9yCnFePD4ImsaAr/sandbox/NA7FxzNaMM0XJxcen4sMS3-images_1771812448684_na1fn_L2hvbWUvdWJ1bnR1L2NvcnJlbGF0aW9uX21hdHJpeA.png?Policy=eyJTdGF0ZW1lbnQiOlt7IlJlc291cmNlIjoiaHR0cHM6Ly9wcml2YXRlLXVzLWVhc3QtMS5tYW51c2Nkbi5jb20vc2Vzc2lvbkZpbGUvSzFtUUpabDl5Q25GZVBENEltc2FBci9zYW5kYm94L05BN0Z4ek5hTU0wWEp4Y2VuNHNNUzMtaW1hZ2VzXzE3NzE4MTI0NDg2ODRfbmExZm5fTDJodmJXVXZkV0oxYm5SMUwyTnZjbkpsYkdGMGFXOXVYMjFoZEhKcGVBLnBuZyIsIkNvbmRpdGlvbiI6eyJEYXRlTGVzc1RoYW4iOnsiQVdTOkVwb2NoVGltZSI6MTc5ODc2MTYwMH19fV19&Key-Pair-Id=K2HSFNDJXOU9YS&Signature=bOXliOxVTb8iKD~vocskFOc5OgkLbG0Qkfjd3XkzOy4NMv2W4mMk4jYfi~bW~-oysrxv4dx9bXWmFEgyvikNOZjyFk-6poGgEk0pMaRoK7pPZSqAMByq5zfMrwNiN--49xv1RauUNby4DSYmw67sN9v27DB8ZQZeEs4~qd5nqOrXAS8yjKqGixPb3XEHdUDllwejqUKTq2lYj7dEY9h1MVcJfWqMZKd9tRcdp5oB1TAM50wPrnOyH4hN4lsb8mVu7JrHXGmNQdC7IibO61XzXrhTtFnb9KcuwRKTrWrESnc1xDu-BPrYmzemgjp2oq8h7KZiNrTViGzS~Np6WHwmJQ__)

#### Resultados da Regressão

O gráfico de dispersão a seguir compara os valores de qualidade do vinho reais com os valores previstos pelo modelo de regressão linear. A linha diagonal representa onde os pontos estariam se as previsões fossem perfeitas.

![Resultados da Regressão](https://private-us-east-1.manuscdn.com/sessionFile/K1mQJZl9yCnFePD4ImsaAr/sandbox/NA7FxzNaMM0XJxcen4sMS3-images_1771812448684_na1fn_L2hvbWUvdWJ1bnR1L3JlZ3Jlc3Npb25fcmVzdWx0cw.png?Policy=eyJTdGF0ZW1lbnQiOlt7IlJlc291cmNlIjoiaHR0cHM6Ly9wcml2YXRlLXVzLWVhc3QtMS5tYW51c2Nkbi5jb20vc2Vzc2lvbkZpbGUvSzFtUUpabDl5Q25GZVBENEltc2FBci9zYW5kYm94L05BN0Z4ek5hTU0wWEp4Y2VuNHNNUzMtaW1hZ2VzXzE3NzE4MTI0NDg2ODRfbmExZm5fTDJodmJXVXZkV0oxYm5SMUwzSmxaM0psYzNOcGIyNWZjbVZ6ZFd4MGN3LnBuZyIsIkNvbmRpdGlvbiI6eyJEYXRlTGVzc1RoYW4iOnsiQVdTOkVwb2NoVGltZSI6MTc5ODc2MTYwMH19fV19&Key-Pair-Id=K2HSFNDJXOU9YS&Signature=NGV2GgPIvuwBgoBINKLuSdnTXtUyKePtb1329TSp4X0G6~Dq50o1-g7zBiMm-zTaKmqEegxRBQEXbQRIRj~10jDVsM6v2Do79VmrpgCKQfBvojRV70QO5G-4vzLvYQP84ZGVGZh0V8RaZht9FYXxEnMhKgORO~qng0HtlHPZHMGP3OBwutqduLqv7VC-oZbvCGm8QWzO-krrGFlvsz13oTF-bEnkQJ~8a4dTz2nAMYIjKF1DkLQZE~ODCCk2hPc4XOYFL3NiDVbC0IR3zbKFkwXKya0hYTMnI2nlPuvW4iSdn2BU-lvgmcvNUgaedKPUgsyMNd86wb2F-Lbr-EnQyA__)

## Conclusão

O modelo de regressão linear desenvolvido explica uma parte da variância na qualidade do vinho com base nas características físico-químicas. Embora o R2 de 0.2598 sugira que outros fatores não incluídos no modelo também influenciam a qualidade, a análise dos coeficientes fornece insights sobre quais características são mais relevantes. A `density` e a `volatile_acidity` mostraram ser as características com maior impacto negativo na qualidade percebida do vinho, enquanto `sulphates`, `pH` e `alcohol` tiveram um impacto positivo. Para melhorar a precisão do modelo, poderiam ser exploradas técnicas de engenharia de características, outros algoritmos de regressão ou a inclusão de variáveis adicionais, se disponíveis.

## Referências

[1]: https://doi.org/10.24432/C56S3T. "Cortez, P., Cerdeira, A., Almeida, F., Matos, T., & Reis, J. (2009). Wine Quality [Dataset]. UCI Machine Learning Repository."

