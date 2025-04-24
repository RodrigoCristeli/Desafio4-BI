# Desafio4-BI

Este projeto faz parte de um Desafio de Projeto voltado à modelagem de dados no Power BI. A proposta consiste em transformar uma tabela única (Financial Sample) em um modelo dimensional baseado em Esquema Estrela (Star Schema), separando as informações em tabelas fato e dimensão para otimizar a análise dos dados.

📊 Objetivo
Aprender a construir um modelo de dados utilizando tabelas fato e dimensão.

Aplicar funções DAX para criação de colunas e medidas.

Melhorar a performance e clareza do modelo por meio de boas práticas de modelagem.

🏗️ Estrutura do Projeto

🔹 Tabela de Origem

Financials_origem: backup oculto da tabela original (modo oculto no modelo).

🔸 Tabelas Dimensão

D_Produtos: contém ID do produto, nome, e estatísticas de vendas (média, mediana, mínimo e máximo).

D_Produtos_Detalhes: detalhes como faixa de desconto, preço de venda, unidades vendidas e custo de fabricação.

D_Descontos: faixa de desconto aplicada por produto.

D_Detalhes: informações complementares não contempladas nas outras dimensões.

D_Calendario: criada via DAX com a função CALENDAR() e enriquecida com colunas como ano, mês, trimestre etc.

🔹 Tabela Fato

F_Vendas: contém os fatos de venda com chave substituta (SK_ID) e chaves estrangeiras ligadas às dimensões.

⚙️ Principais Etapas

Importação da Tabela Original

Utilização do Financial Sample como base única para o modelo.

Criação das Tabelas Dimensão e Fato

Feita através de referência e transformação no Power Query.

Agrupamentos, remoção de duplicatas e cálculos de estatísticas com colunas calculadas.

Modelagem Relacional

Conexão das tabelas por chaves primárias e estrangeiras, formando o Esquema Estrela.

Criação de Colunas Calculadas e Medidas com DAX

Uso de funções como CALCULATE, SUMX, MEDIANX, FORMAT, entre outras.

Aplicação de lógica condicional para criação de colunas como índice de produto.

🧠 DAX Utilizado

CALENDAR(): criação da tabela D_Calendario.

YEAR(), MONTH(), FORMAT(): extração de componentes da data.

CALCULATE(), AVERAGEX(), MEDIANX(), MINX(), MAXX(): cálculo de estatísticas.

SWITCH() / IF(): criação de colunas condicionais e categorização.

🖼️ Esquema em Estrela

📌 Salve uma imagem do diagrama no Power BI e inclua aqui no repositório.

💾 Como Executar

Baixe ou clone este repositório.

Abra o arquivo Modelo_Estrela_FinancialSample.pbix no Power BI Desktop.

Explore o modelo, as relações e medidas DAX.

🚀 Conclusão

Este projeto demonstra a construção de um modelo de dados eficiente, utilizando boas práticas de modelagem dimensional no Power BI, com foco em organização, performance e capacidade analítica.

📚 Aprendizados

Modelagem dimensional com Esquema Estrela.

Manipulação de dados no Power Query.

Criação de tabelas e colunas com DAX.

Otimização de visualizações e análise de dados no Power BI.
