# House Rocket Project

Este é um projeto fictício. A empresa, o contexto e as perguntas de negócios não são reais. Este portfólio está seguindo as recomendações do blog [Seja um Data Scientist](https://sejaumdatascientist.com/os-5-projetos-de-data-science-que-fara-o-recrutador-olhar-para-voce/) 


# 1. Descrição 

House Rocket é uma empresa do ramo imobiliario que procura novos imóveis para seu catalogo, fomentada pela alta e baixa recorrente do mercado imobiliário a empresa busca novas oportunidades de compra de imóveis. A empresa procurou um Cientista de dados para ajudar a encontrar as melhores oportunidades de negócio, ou seja, maximizar a receita. A melhor estratégia é a compra de casas em condições regulares quando estiverem em baixa no mercado e revende-las quando o mercado estiver em alta. Os atributos das casas as tornam mais ou menos atrativas, influenciando a atratividade dos imóveis e, consequentemente, o seu preço. As questões a serem respondidas são:

**1**. Quais casas o CEO da House Rocket deveria comprar e por qual preço de compra?

**2.** Uma vez a casa em posse da empresa, qual o melhor momento para vendê-las e qual seria o preço da venda?

 


# 2. Atributos 

Os dados para este projeto podem ser encontrados em: https://www.kaggle.com/harlfoxem/housesalesprediction/discussion/207885 . Abaixo segue a definição para cada um dos 21 atributos:


|    Atributos    |                         Significado                          |
| :-------------: | :----------------------------------------------------------: |
|       id        |       Numeração única de identificação de cada imóvel        |
|      date       |                    Data da venda da casa                     |
|      price      |    Preço que a casa está sendo vendida pelo proprietário     |
|    bedrooms     |                      Número de quartos                       |
|    bathrooms    | Número de banheiros (0.5 = banheiro em um quarto, mas sem chuveiro) |
|   sqft_living   | Medida (em pés quadrado) do espaço interior dos apartamentos |
|    sqft_lot     |     Medida (em pés quadrado) quadrada do espaço terrestre     |
|     floors      |                 Número de andares do imóvel                  |
|   waterfront    | Variável que indica a presença ou não de vista para água (0 = não e 1 = sim) |
|      view       | Um índice de 0 a 4 que indica a qualidade da vista da propriedade. Varia de 0 a 4, onde: 0 = baixa  4 = alta |
|    condition    | Um índice de 1 a 5 que indica a condição da casa. Varia de 1 a 5, onde: 1 = baixo \|-\| 5 = alta |
|      grade      | Um índice de 1 a 13 que indica a construção e o design do edifício. Varia de 1 a 13, onde: 1-3 = baixo, 7 = médio e 11-13 = alta |
|  sqft_basement  | A metragem quadrada do espaço habitacional interior acima do nível do solo |
|    yr_built     |               Ano de construção de cada imóvel               |
|  yr_renovated   |                Ano de reforma de cada imóvel                 |
|     zipcode     |                         CEP da casa                          |
|       lat       |                           Latitude                           |
|      long       |                          Longitude                           |
| sqft_livining15 | Medida (em pés quadrado) do espaço interno de habitação para os 15 vizinhos mais próximo |
|   sqft_lot15    | Medida (em pés quadrado) dos lotes de terra dos 15 vizinhos mais próximo |



# 3. Premissas do Negócio
  As seguintes premissas foram consideradas para esse projeto:
- Os valores iguais a zero em **yr_renovated** são casas que nunca foram reformadas.
- O valor igual a 33 na coluna **bathroom** foi considerada um erro e por isso foi delatada das análises
- Os valores não inteiros nos atributos **bathrooms** e **floors** foram arrendados com o intuito de simplificar o projeto.
- A coluna **price** significa o preço que a casa foi / será comprada pela empresa House Rocket
- A localidade e a condição do imóvel foram características decisivas na compra ou não do imóvel


# 4. Estratégia de solução

Quais foram as etapas para solucionar o problema de negócio:

1. Coleta de dados via Kaggle

2. Entendimento de negócio

3. Tratamento de dados 

3.1. ​	Tranformação de variaveis 

3.2. ​	Limpeza 

3.3. ​	Entendimento

4. Exploração de dados

5. Responder problemas do negócio

6. Resultados para o negócio

7. Conclusão

# 5. Top Insights

Insights mais relevantes para o projeto:

Imóveis com vista pra água são em média 300% mais caros, mas curiosamente dos imóveis selecionados pelos nossos filtros, a diferença cai para 30%

Imóveis que nunca sofreram reformas são 30.25% mais baratos que os imóveis que ja sofreram algum tipo de reforma.

Imóveis com 5-8 quartos são mais caros sendo,43% mais caros se comparado a imóveis com 9 a 11 quartos,  e 89.27% mais caros se comparados a imóveis com 0 a 3 quartos.




# 6. Tradução para o negócio

O que as análises das hipóteses dizem sobre o negócio.

| Hipótese                                                     | Resultado  | Tradução para negócio                                        |
| ------------------------------------------------------------ | ---------- | ------------------------------------------------------------ |
| **H1** -Imóveis com vista para a água são em média 30% mais caros | Verdadeira | Investir em imóveis com vista para água                      |
| **H2** - Imóveis com data de construção menor que 1955 são em média 50% mais baratos | Falsa      | Investir em imóveis independente da data de construção       |
| **H3** - Imóveis sem porão são 40% maiores do que imóveis com porão | Verdadeira | Investir em imóveis sem porão                                |
| **H4** - Imóveis que nunca foram reformados são em média 20% mais baratos | Verdadeira | Investir em imóveis não reformados e reformá-los para venda  |
| **H5** - Imóveis com mais banheiros são em média 15% mais caros | Falsa      | Investir em imóveis de até 3 banheiros                         |
| **H6** - Imóveis com mais quartos são em média 15% mais caros   | Falsa      | Investir em imóveis de até 3 quartos                  |
| **H7** - O crescimento do preço dos imóveis mês após mês no ano de 2014 é de 10% | Falsa      | Investir em imóveis nos meses de menor custo                 |
| **H8** - O crescimento do preço dos imóveis ano após ano é de 10% | Falsa      | Investir em imóveis nos anos de menor custo                 |





Ao final do estudo foi sugerido os 20 imóveis mais lucrativos para a empresa adquirir.

|        |                         Valor USD                        |
| :-------------: | :----------------------------------------------------------: |
|     Investimento inicial       |       15215317        |
|     **Lucro Esperado**      |                    14540533                    |





# 7. Conclusão

Os objetivos foram alcançados. Os imóveis foram agrupados por região (zipcode). Considerando o preço do imóvel, que deveria estar abaixo da média da região e a condição minima como regular (3 - 5) foi calculado a mediana do preço. Ao total 10579 imóveis foram declarados como Imóveis com alto potencial de revenda, dentre estes foram sugeridos os 20 mais lucrativos para a empresa comprar. Segundo a estimativa, desses 20 imóveis o potencial de lucro é de aproximadamente 95% sobre o valor investido.

Para o futuro seria interessante analisar o potencial de lucratividade atraves de reformas para alguns imóveis baseados em sua localização, comprando imóveis em condições ruins, reformando-os e revendendo-os com finalidade de avaliar qual tipo de reforma retornaria lucro para a empresa. Outra ideia seria a possibilidade de prever a valorização do imóvel.

