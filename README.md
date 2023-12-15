# circularidade_medica_rede_neural

Avaliação Comparativa de Modelos de Rede Neural e Tradicionais para Classificação no Problema de Circularidade Médica no Brasil

A problemática da circularidade médica aborda a dinâmica de deslocamento de profissionais de saúde em relação à distribuição geográfica dos locais de atendimento. Essa questão assume grande relevância diante da persistente escassez de médicos em determinadas regiões do Brasil, geralmente associadas a índices de desenvolvimento humano mais baixos ou localidades mais remotas. 

Neste projeto, nosso objetivo é empregar as informações disponíveis na base de dados para realizar a classificação do local onde um novo estudante possivelmente irá cursar medicina, com base em suas características. Para atingir esse fim, exploramos três abordagens de classificação por meio de aprendizado de máquina supervisionado: o Random Forest, como um classificador convencional; uma rede neural utilizando o Perceptron; e uma rede neural implementada com a biblioteca TensorFlow.

A avaliação de desempenho desses modelos em um conjunto de teste proporcionou uma comparação robusta de seus resultados. O intuito final é criar um sistema preditivo capaz de antecipar o código do estado onde o estudante provavelmente escolherá cursar medicina, utilizando as informações contidas na base de dados como guia para essa previsão.

Os resultados obtidos indicam que a rede neural superou o Random Forest, ilustrando a importância da escolha adequada de técnicas e modelos a serem utilizados. Este projeto utiliza dados fornecidos pelo Sistema Único de Saúde (SUS) e Instituto Nacional de Estudos e Pesquisas (INEP), dados que já estão devidamente rotulados, permitindo uma avaliação sólida dos modelos em uma coleção categorizada. Por conter dados sensiveis a base de dados não pode ser compartlihada. Mas para reproduzir o projeto é preciso ter uma base com as seguintes caracteristicas, sendo a coluna de co_uf_ies o nosso alvo.

| Nome | Tipo | Descrição |
|-------|-----|-------------|
| idade | int | Idade do individuo    |
| sexo  | int | Sexo do individuo. Definido como 0 ou 1, onde 0 é masculino e 1 é feminino   |
| raca  | int | Cor ou raça declarada pelo indivíduo, pode ser definida como 0:Não declarado, 1:Branco, 2:Preto, 3:Marrom, 4:Amarelo, 5:Indígena, 6:Nenhuma informação disponível    |
| co_uf_nasc | int | Código IBGE do estado onde o indivíduo foi registrado    |
| co_uf_ies  | int | Código IBGE do estado onde o indivíduo estudou medicina   |
| idh_uf_nasc | int | Valor do índice de desenvolvimento humano do estado onde o indivíduo foi registrado    |
| idh_uf_ies  | int | Valor do índice de desenvolvimento humano do estado onde o indivíduo estudou    |
| dist  | int | istância entre a cidade onde o indivíduo nasceu e a cidade onde estudou medicina    |

