# Balanço de compras e vendas

Apesar de ser um conjunto de dados pequeno, foram adquiridos diversos conceitos importantes de ETL durante o tratamento desses dados.

## Etapas do tratamento de dados

1. Unir a Tabela de Compras com a Tabela de Vendas para que todos os códigos contábeis e setores estivejam disponíveis em apenas uma tabela;
2. Criar as tabelas dimSetor e dimCOD Contábil por meio da filtragem de itens únicos da tabela criada anteriormente;
3. Criar a tabela dimData;
 
   Para criar a tabela dimData foi criada uma nova consulta e utilizada a função List.Dates(), em seguida foram criadas variáveis para substituir os parâmetros da função            List.Dates(), conforme pode ser visto abaixo:
 
   ![image](https://user-images.githubusercontent.com/81938273/148427428-5f7e38fb-f422-4593-9dec-21507826e2c0.png)
 
    Dessa forma é possível criar uma tabela de dimensão Data que vai do primeiro dia do primeiro ano presente nos dados, até o último dia do último ano.

4. Criar as tabelas ftCompras e ftVendas. Nesta etapa foi realizado a mesclagem das tabelas ft com as tabelas dim, com a finalidade de utilizar apenas o Id das dimensões na tabela ft;
5. Organizar as tabelas em pastas e desabilitar a carga das tabelas auxiliares para dentro do Power BI;
6. Gerenciar as relações entre as tabelas e linkar corretamente os Id's das tabelas dimensão com os Id's das tabelas fato, configurando relações 1xN em todas as relações, conforme apresentado no esquema abaixo.

![image](https://user-images.githubusercontent.com/81938273/148430813-2b580ddf-b4f1-4def-97e0-bffff04f2713.png)


