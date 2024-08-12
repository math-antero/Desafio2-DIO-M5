# Desafio2-DIO-M5

Descrição do Desafio de Projeto
Utilizaremos a tabela única de Financial Sample para criar as tabelas dimensão e fato do nosso modelo baseado em star schema. O processo consiste na criação das tabelas com base na tabela original. A partir da cópia serão selecionadas as colunas que irão compor a visão da nova tabela.
1. Tabela D_Produto: Para a criação dessa tabela utilizei a função "AGRUPAR POR" do power query, onde foram criadas colunas para exibir os dados exigidos como uma coluna com a soma de todas as unidades vendidas, outa com a média de valor de vendas, valo mínimo de venda, valor máximo de venda, entre outros dados;
2. Na criação das demais tabelas foi utilizado apenas a seleção dos dados nescessários para cada uma das tabelas e exclusão das demais colunas.
3. Foi feito também a criação da coluna ID_Produto em todas as tabelas para conseguir realizar os relacionamentos de forma saudável e evitando a repetição de colunas desnecessárias;
4. Depois, através da linguagem DAX, foi criada uma tabela calendário com os seguintes dados:
      I. Date - Comando: DATE = CALENDARAUTO(12);
      II. Year - Comando: Year = YEAR(D_Calendar[DATE]);
      III. Month Number - Comando: Month Number = MONTH(D_Calendar[DATE]);
      IV. Week Number - Comando: Week Number = WEEKNUM(D_Calendar[DATE]);
      V. Day of the week - Comando: Day of the week = WEEKDAY(D_Calendar[DATE]);
      VI. Day of the week2 - Comando: Day of the week2 = FORMAT(D_Calendar[DATE], "DDDD");

Star Schema montado através das tabelas:

![Desafio 2 - M5](https://github.com/user-attachments/assets/955588f2-fb08-4631-aa5d-025700a83e5f)



6. Por fim, foi montado os Star Schema onde as tabelas de dimensão são relacionadas com a tabela fato.
