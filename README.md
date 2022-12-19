<img src='https://thumbs.jusbr.com/filters:format(webp)/imgs.jusbr.com/publications/images/ee45e13d4120d57ffac4899188220bce'/>

[![forthebadge made-with-python](http://ForTheBadge.com/images/badges/made-with-python.svg)](https://www.python.org/)
[![forthebadge Pandas](https://img.shields.io/badge/Codecov-F01F7A?style=for-the-badge&logo=Codecov&logoColor=white]


# Cury-Delivery-Food-Insights
## 1. Business assumptions
A Cury Company é uma empresa de tecnologia que criou um aplicativo que conecta restaurantes, entregadores e pessoas.

Através desse aplicativo, é possível realizar o pedido de uma refeição, em qualquer restaurante cadastrado, e recebê-lo no conforto da sua casa por um entregador também cadastrado no aplicativo da Cury Company.

A empresa realiza negócios entre restaurantes, entregadores e pessoas, e gera muitos dados sobre entregas, tipos de pedidos, condições climáticas, avaliação dos entregadores e etc. Apesar da entrega estar crescento, em termos de entregas, o CEO não tem visibilidade completa dos KPIs de crescimento da empresa.

A minha ideia como cientista de dados é a de criar soluções à necessidade da empresa, que é de ter um alguns KPIs estratégicos organizados em uma única ferramenta, para que o CEO possa consultar e conseguir tomar decisões simples, porém importantes. Partindo dessa solução, poderei pensar em alguns algoritmos para solucionar problemas mais complexos do negócio.

A Cury Company possui um modelo de negócio chamado Marketplace, que fazer o intermédio do negócio entre três clientes principais:
- Restaurantes;
- entregadores; e
- e pessoas compradoras.## 

# 2. Perguntas do negócio 

As questões a serem respondidas com a abordagem de Análise Exploratória de Dados - EDA são:

### 2.1. Do lado da Empresa:

**1**. Quantidade de pedidos por dia.

**2**. Quantidade de pedidos por semana.

**3**. Distribuição dos pedidos por tipo de tráfego.

**4**. Comparação do volume de pedidos por cidade e tipo de tráfego.

**5**. A quantidade de pedidos por entregador por semana.

**6**. A localização central de cada cidade por tipo de tráfego.

## 2.2. Do lado dos entregadores

**1**. A menor e maior idade dos entregadores.

**2**. A pior e a melhor condição de veículos.

**3**. A avaliação médida por entregador.

**4**. A avaliação média e o desvio padrão por tipo de tráfego.

**5**. A avaliação média e o desvio padrão por condições climáticas.

**6**. Os 10 entregadores mais rápidos por cidade.

**7**. Os 10 entregadores mais lentos por cidade.

## 2.3. Do lado dos Restaurantes

**1**. A quantidade de entregadores únicos.

**2**. A distância média dos resturantes e dos locais de entrega.

**3**. O tempo médio e o desvio padrão de entrega por cidade.

**4**. O tempo médio e o desvio padrão de entrega por cidade e tipo de pedido.

**5**. O tempo médio e o desvio padrão de entrega por cidade e tipo de tráfego.

**6**. O tempo médio de entrega durantes os Festivais.


# 3. Atributos 

Os dados para este projeto podem ser encontrados em: https://www.kaggle.com/datasets/gauravmalik26/food-delivery-dataset?select=train.csv. Abaixo segue a definição para cada um dos 20 atributos, entendendo que cada atributo trata-se de 1 coluna da base de dados:


|    Atributos    |                         Significado                          |
| :-------------: | :----------------------------------------------------------: |
|       id        |       Numeração única de identificação de cada entrega realizada        |
|Delivery_person_ID       |                    É a identificação do entregador de cada entrega                     |
|Delivery_person_Age      |    É a idade do entregador de cada entrega    |
|Delivery_person_Ratings     | É a nota dada ao entregador de cada entrega                       |
|Restaurant_latitude    | A latitude geoespacial do restaurante que fez a entrega |
|Restaurant_longitude   | A longitude geoespacial do restaurante que fez a entrega |
|Delivery_location_latitude     |     A latitude geoespacial de onde foi feita a entrega     |
|Delivery_location_longitude      |  A latitude geoespacial de onde foi feita a entrega                  |
|Order_Date       |  Data do pedido e entrega realizada  |
|Time_Orderd             | Hora do pedido  |
|  Time_Order_picked      | Hora da retirada do pedido realizada pelo entregador |
|  Weatherconditions          | Condição climática do período da entrega |
| Road_traffic_density   |Condição do trânsito no período da entrega  |
|  Vehicle_condition       |  Condição e estado do veículo utilizado para a entrega                            |
| Type_of_order	    |  Tipo do pedido realizado                               |
|  Type_of_vehicle        |  Tipo do veículo utilizado para a entrega                                                 |
| multiple_deliveries             | Informação da quantidade de entregas realizadas pelo entregador juntamente com esse pedido        |
|  Festival           |  Período de festas e eventos da cidade                                                   |
| City | Cidade do pedido e entrega |
| Time_taken(min)      | Tempo desde a retirada do pedido no restaurante até a entrega na casa do cliente |
| Week_of_year      | Semana do ano |
| Delivery_distance      | Distância entre o restaurante e o local do cliente |


# 4. Premissas do Negócio
  As seguintes premissas foram consideradas para esse projeto:
- Os valores 'NaN' encontrados nas colunas foram substituídos pela média dos valores e não foram excluídos;
- Foram encontrados e retirados espaçamentos do nosso dataset, espaçamentos estes que prejudicariam as nossas análises;
- não foi possível, com as informações disponíveis, o estabelecimento de critérios que, de forma eficiente, nos desse uma posição exata dos melhores e piores entregadores;
- As condições do trânsito, bem como o tipo de veículo são decisivos para a velocidade da entrega. Contudo, não é possível, com as informações disponíveis, o estabelecimento de critérios eficientes para sabermos a real situação da relação acima estabelecida entre tipo de veículo, distância e condição climática.


# 5. Estratégia de solução

Quais foram as etapas para solucionar o problema de negócio:

1. Coleta de dados via Kaggle

2. Entendimento de negócio

3. Tratamento de dados 

3.1. ​	Tranformação de variaveis 

3.2. ​	Limpeza 

3.3. ​	Entendimento

4. Exploração de dados

5. Responder problemas do negócio

6. Conclusão


# 6. Top Insights

Insights mais relevantes para o projeto e que auxilia a Cury - Delivery Food na tomada de decisões importantes ao negócio são (acionáveis):

Imóveis com vista pra água são em média 300% mais caros

Imóveis que nunca sofreram reformas são 30.21% mais baratos que os imóveis que ja sofreram algum tipo de reforma.

Imóveis com 6-9 quartos são mais caros sendo,149% mais caros se comparado a imóveis com 0 a 3 quartos, 48.9% mais caros se comparados a imóveis com 3 a 6 quartos e 107% mais caros se comparados a imóveis com 9 a 11 quartos.




# 7. Tradução para o negócio

O que as análises das hipóteses dizem sobre o negócio.

| Hipótese                                                     | Resultado  | Tradução para negócio                                        |
| ------------------------------------------------------------ | ---------- | ------------------------------------------------------------ |
| **H1** -Imóveis com vista para a água são em média 30% mais caros | Verdadeira | Investir em imóveis com vista para água                      |
| **H2** - Imóveis com data de construção menor que 1955 são em média 50% mais baratos | Falsa      | Investir em imóveis independente da data de construção       |
| **H3** - Imóveis sem porão são 40% maiores do que imóveis com porão | Verdadeira | Investir em imóveis sem porão                                |
| **H4** - Imóveis que nunca foram reformados são em média 20% mais baratos | Verdadeira | Investir em imóveis não reformados e reformá-los para venda  |
| **H5** - Imóveis com mais banheiros são em média 15% mais caros | Falsa      | Investir em imóveis de 3-5 banheiros                         |
| **H6** - Imóveis com mais quartos são em média 15% mais caros   | Falsa      | Investir em imóveis com 6-9 quartos                  |
| **H7** - O crescimento do preço dos imóveis mês após mês no ano de 2014 é de 10% | Falsa      | Investir em imóveis nos meses de menor custo                 |
| **H8** - O crescimento do preço dos imóveis ano após ano é de 10% | Falsa      | Investir em imóveis nos anos de menor custo                 |




Ao final do estudo foi sugerido os 20 imóveis mais lucrativos para a empresa adquirir.

|        |                         Valor USD                        |
| :-------------: | :----------------------------------------------------------: |
|     Investimento inicial       |       6889600        |
|     **Lucro Esperado**      |                    2066880                    |





# 8. Conclusão

Os objetivos foram alcançados. Os imóveis foram agrupados por região (zipcode). Considerando o preço do imóvel e a condição minima como regular (3 - 5) foi calculado a mediana do preço. Ao total 10505 imóveis foram declarados como Imóveis com alto potencial de revenda, dentre estes foram sugeridos os 20 mais lucrativos para a empresa comprar. Os imóveis aptos para compra foram agrupados pela localidade e a estação do ano. A mediana foi calculada e imóveis com preço abaixo da mediana teve um acréscimo de 10% em seu valor, enquanto imóveis com preço acima da mediana teve um acréscimo de 30% acima do seu valor. 

Para o futuro seria interessante analisar o potencial de lucratividade atraves de reformas para alguns imóveis baseados em sua localização, comprando imóveis em condições ruins, reformando-os e revendendo-os com finalidade de avaliar qual tipo de reforma retornaria lucro para a empresa. Outra ideia seria a possibilidade de prever a valorização do imóvel, tirando o limitando de 4 estações para os valores dos imóveis, possibilitando uma margem de lucro maior.

