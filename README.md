# Projeto 1: "Problema de negócio - Precificação de veículos usados"

## Introdução

![Alt ou título da imagem](https://raw.githubusercontent.com/Campos-Silva/Projeto_1_Precificacao_de_Veiculos_Usados/main/comprar_carro_duvida_c.png)

Quando vamos comprar um carro usado uma das primeiras questões que devemos checar é se o preço está de acordo com as características do veículo. Esse tipo de pensamento deve valer também ao vendedor. Agências que compram veículos usados ou seminovos para revender precisam comprá-los com preços condizentes as suas características, isso para que possam ter lucro nessas revendas. Assim, saber quanto vale um veículo não é uma questão trivial, e sim uma questão que influencia nas nossas tomadas de decisão (ENGERS; HARTMANN; STERN, 2009; OU et al., 2020).

![Alt ou título da imagem](https://raw.githubusercontent.com/Campos-Silva/Projeto_1_Precificacao_de_Veiculos_Usados/main/Apresenta%C3%A7%C3%A3o1_b.png)

Essa questão é ainda mais importante nos dias de hoje, uma vez que o setor de negócios de compra e venda de veículos está em alta. No Brasil, a venda de carros usados e seminovos tiveram cerca de 8% a mais de vendas acumuladas quando comparadas com o mesmo período de 2019, período anterior a pandemia (FOLHA, 2021 , FENAUTO, 2021). Já os primeiros sete meses de 2021 tiveram acréscimo de vendas acumuladas de 55%, em comparação com o mesmo período de 2020 (FOLHA, 2021). Esse cenário se deve, em grande medida, ao fato de que a pandemia do COVID-19 tem impactado negativamente o fluxo de produção das montadoras, o que ocasionou em 2020 a que queda de 32% de venda de carros novos (El PAÍS, 2021, FENAUTO, 2021). Dessa forma, a criação de um modelo preditivo, também conhecido como Modelo de Machine Learning, que balanceie adequadamente o preço de veículos usados e seminovos, para que nem o comprador e nem o vendedor sejam prejudicados, é assim necessário uma vez que possibilita que tomemos decisões baseadas em dados. Além de que é o cerne da questão desse setor de negócios que faz girar grande quantidade de recursos financeiros em todo o mundo.

![Alt ou título da imagem](https://raw.githubusercontent.com/Campos-Silva/Projeto_1_Precificacao_de_Veiculos_Usados/main/carro_variaveis_e.png)

Encontrar "quais" caracteristicas influenciam e "como" elas direcionam a precificação de veículo são questões chaves nesse setor de negócios. Características como a quilometragem, a idade do carro, o consumo médio têm sido descrito como influenciadoras dessa precificação (ENGERS; HARTMANN; STERN, 2009; MONBURINON et al., 2018). Porém, as características podem influenciar diferentemente nessa precificação. Por exemplo, para certos modelos, quanto mais recente for o veículo mais alto tenderá a ser o seu valor. Por outro lado, veículos com maior quilometragem e maior consumo médio de combustível tendem a possuir menor preço. Dessa forma, analisar como as características direcionam o preço do veículo é também importante.

## Objetivo, hipótese e previsão

![Alt ou título da imagem](https://raw.githubusercontent.com/Campos-Silva/Projeto_1_Precificacao_de_Veiculos_Usados/main/alvo_b.png)

É nesse contexto que objetivei construir um Modelo de Machine Learning que atuasse na previsão de preços de veículos usados baseados em suas características. Para este projeto utilizei duas características dos veículos, que são (1) a quilometragem total do carro e (2) o consumo médio. A hipótese é que ambas as caracteristicas influenciam no preço. Já a previsão é de que quanto maior for a quilometragem e o consumo de combustível do veículo, menor será o preço do veículo.

![Alt ou título da imagem](https://raw.githubusercontent.com/Campos-Silva/Projeto_1_Precificacao_de_Veiculos_Usados/main/importancia.jpg)

O modelo preditivo permitirá a tomada de decisões que visem a maximização dos lucros e redução de perdas por meio da precificação do veículo baseado em suas caractersticas. Dessa forma, o modelo de Machine Learning sugerido aqui será importante para a tomada de decisões orientadas em dados, e por exemplo, poderá ser empregada tanto por agências revendedoras de veículos usados, como para pessoas que querem comprar ou vender veículos usados.

## Material e métodos

### Detalhamento do conjunto de dados

![Alt ou título da imagem](https://raw.githubusercontent.com/Campos-Silva/Projeto_1_Precificacao_de_Veiculos_Usados/main/anotacao_b.png)

Para fins didáticos eu separei esse projeto em quatro partes. Cada parte contêm uma etapa essencial dos trabalhos de Data Science que são:

- ["Parte A: Importação e limpeza dos dados"](https://github.com/Campos-Silva/Projeto_01_Parte_A_Importacao-e-limpeza-de-dados-no-Python);

- ["Parte B: Exploração dos dados"](https://github.com/Campos-Silva/Projeto_01_Parte_B_Exploracao_de_dados_no_Python);

- ["Parte C: Construção e avaliação de Modelos de Machine Learning"](https://github.com/Campos-Silva/Projeto_01_Parte_C_Modelos_de_Machine_Learning_no_Python);

- ["Parte D: Modelo em Produção"](https://github.com/Campos-Silva/deploy_carros_streamlit).

## Resultados

![Alt ou título da imagem](https://raw.githubusercontent.com/Campos-Silva/Projeto_1_Precificacao_de_Veiculos_Usados/main/resultados_b.jpg)

O modelo escolhido foi o modelo combinado obtido através da função 'blend_models" do pycaret, cujos valores de métricas de erro para o método de validação são de 0.25 para o RMSLE e 872.00 para o Erro Absoluto Médio . Esse último valor tem grande significância para a área de negócio, uma vez que expressa que esse "melhor modelo" tem um erro médio, tanto para cima como para baixo, de cerca de 872 dólares.

## Discussão

![Alt ou título da imagem](https://raw.githubusercontent.com/Campos-Silva/Projeto_1_Precificacao_de_Veiculos_Usados/main/discussao_b.jpg)

Esse modelo final permite que veículos usados e seminovos sejam precificados de forma baseada em um conjunto de dados do setor de negócios, o qual servirá como guia na tomada de decisões orientadas em dados, fator essencial para empresas (PROVOST; FAWCETT, 2016). O uso do modelo permite, por exemplo, que uma agência decida se compra ou não um veículo de terceiros baseado nas caracteristicas do veículo e seu preço repassado pelo terceiro. Caso o preço repassado a ela seja similar ou dentro da faixa de erro desse modelo (entre $872,00) a agência, se fechar acordo de compra, poderá lucrar na revenda ao vender por um preço maior do que ela comprou. Além disso, essa mesma agência poderá ter clientes mais satisfeitos uma vez que não estará cobrando preços abusivos na revenda de veículos. Isso porque baseará a precificação em tabelas de preços adequadas com as caracteristicas do veículo. Isso poderá trazer vantagens competitivas a essa agência frente a outras do mesmo setor de negócios (PROVOST; FAWCETT, 2016).

Dessa forma, o modelo serve como guia para a tomada de decisões, não baseada em intuição, mas sim orientadas em dados. E ainda assim, esse modelo preditivo beneficiará tanto comprador como vendedor. Uma vez que esse setor de negócios gira grandes quantidades de recursos financeiros em todo o mundo a tomada de decisões baseada em análises preditivas, como as obtidas por esse modelo, possibiita que seja maximizada os lucros finais nesse setor como um todo.


## Conclusão

![Alt ou título da imagem](https://raw.githubusercontent.com/Campos-Silva/Projeto_1_Precificacao_de_Veiculos_Usados/main/carro_venda_c.jpg)

O setor de negócios de compra e venda de veículos usados e seminovos está em pleno crescimento no Brasil atualmente, e é uma área que movimenta grande quantidade de recursos financeiros em todo o mundo. O fornecimento de modelos preditivos que associem o preço desses veículos as suas caracteristicas permite maximização dos lucros e minimização de perdas ocasionados pela não cotação adequada desse preço ao respectivo veículo. Dessa forma, esse modelo preditivo aqui criado possibilita servir como um guia na precificação, sendo importante ferramenta para essa área de negócios.

____


## Autor:

<img  src="https://raw.githubusercontent.com/Campos-Silva/Campos-Silva/main/perfil_lucas_andrei_campos_silva.png" width="80" alt="cognitiveclass.ai logo" align="left" /> 

### &nbsp;&nbsp;Lucas Andrei Campos-Siva

<p>
&nbsp;&nbsp;Cientista de Dados / Business Intelligence / Analista de Dados<br/>
&nbsp;&nbsp;LinkedIn: https://www.linkedin.com/in/lucas-andrei-campos-silva/<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;E-mail: ds.campossilva@gmail.com<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Portifólio de projetos em Data Science: https://github.com/Campos-Silva
</p>

____

## Referências Bibliográficas

- EL PAÍS. Furor no mercado de carros usados e na construção civil expõe as bolhas econômicas no Brasil da pandemia. 2021. Available at: https://brasil.elpais.com/economia/2021-05-24/furor-no-mercado-de-carros-usados-e-na-construcao-civil-expoe-as-bolhas-economicas-no-brasil-da-pandemia.html.

- ENGERS, MAXIM; HARTMANN, MONICA; STERN, STEVEN. ANNUAL MILES DRIVE USED CAR PRICES. J. Appl. Econ, vol. 24, p. 1–33, 2009. https://doi.org/10.1002/jae. FENAUTO. Vendas de carros usados mantêm viés positivo. 2021. Available at: https://www.fenauto.org.br/index.php?view=single&post_id=895.

- FOLHA. Venda de carros usados cresce 55 % no Brasil em 2021. 2021. Available at: https://estudio.folha.uol.com.br/conectaauto/2021/10/olx-lanca-conecta-autos-evento-online-e-gratuito-para-profissionais-do-mercado-automotivo.shtml.

- MONBURINON, Nitis; CHERTCHOM, Prajak; KAEWKIRIYA, Thongchai; RUNGPHEUNG, Suwat; BUYA, Sabir; BOONPOU, Pitchayakit. Prediction of Prices for Used Car by Using Regression Models. 2018. Proceedings of 2018 5th International Conference on Business and Industrial Research: Smart Technology for Next Generation of Information, Engineering, Business and Social Science, ICBIR 2018. Bangkok: IEEE, 2018. p. 115–119. https://doi.org/10.1109/ICBIR.2018.8391177.

- OU, Shiqi; LI, Wan; LI, Jie; LIN, Zhenhong; HE, Xin; BOUCHARD, Jessey; PRZESMITZKI, Steven. Relationships between vehicle pricing and features: Data driven analysis of the Chinese vehicle market. Energies, vol. 13, no. 12, p. 1–25, 2020. https://doi.org/10.3390/en13123088.
PROVOST, Foster; FAWCETT, Tom. Data Science para Negócios. 1a. Rio de Janeiro: Alta Books, 2016.

- UFPR. Método de Reamostragem. 2021. Available at: http://cursos.leg.ufpr.br/ML4all/apoio/reamostragem.html.
