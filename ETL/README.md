# Descrição do desafio:
Processamento de dados simplificado com Power BI. Os arquivos de dados disponíveis estão no GitHub: https://github.com/julianazanelatto/power_bi_analyst/tree/main/M%C3%B3dulo%203/Desafio%20de%20Projeto

## Diretrizes:

1 Preparação do ambiente:

1.1 Criar uma instância no Azure para MySQL ✅

<img width="964" alt="image" src="https://github.com/Renatamoreirac/Dio-pbi/assets/147671867/346acd0c-d0de-47c4-a262-fcb08ad1ab62">

![image](https://github.com/Renatamoreirac/Dio-pbi/assets/147671867/87d4fd25-a65d-45df-a943-ac64bb436b0a)

1.2 Criar o Banco de Dados disponível no GitHub ✅

![image](https://github.com/Renatamoreirac/Dio-pbi/assets/147671867/ceee2708-1053-4cba-9e65-d487c63d4c17)


1.3 Integrar o Power BI com o MySQL no Azure ✅

1.4 Verifique problemas na base a fim de realizar a transformação dos dados ✅

## Transformação dos dados:
1. Verifique os cabeçalhos e tipos de dados ✅
2. Modificar os valores monetários para o tipo duplo preciso ✅: Alterada o tipo de dato para número decimal fixo na coluna Salary. 
3. Verificar a existência de nulos e analisar a remoção ✅: Há apenas um valor null na tabela employee na coluna Super_Ssn
4. Os funcionários com nulos em Super_ssn podem ser os gerentes ✅:Verifique se há algum colaborador sem gerente: Sim, o calaborador James de SSn: 888665555
5. Verifique se há algum departamento sem gerente ✅: Verificado que todos tem gerente
6. Se houver departamento sem gerente, suponha que você possua os dados e preencha as lacunas✅
7. Verifique o número de horas dos projetos ✅: Substituido ponto por vígula para adequação do tipo de dado 
8. Separar colunas complexas ✅: separado endereço 
9. Mesclar consultas funcionário e departamento para criar uma tabela funcionário com o nome dos departamentos associados aos colaboradores. A mescla terá como base a tabela funcionário ✅: Realizado a mesclagem (inner join) em uma nova tabela nomeada como funcionario apartir da chave estrangeira Dno da tabela employee e a chave primária Dnumber da tabela departament. 
10. Neste processo elimine as cargas desnecessárias ✅
11. Realizar o gerente dos colaboradores e os nomes dos colaboradores. Isso pode ser feito com consulta SQL ou mesclando tabelas com Power BI ✅: feito na tabela funcionários
12. Mesclar as colunas de Nome e Sobrenome para ter apenas uma coluna definindo os nomes dos colaboradores ✅   
14. Mesclar os nomes dos departamentos e localização. Isso fará com que cada combinação departamento-local seja única ✅
15. Agrupar os dados a fim de saber quantos colaboradores existem por gerente ✅: Realizado na tabela departamento a mesclagem e logo depois uma agregação para contagem de colaboradores para cada gerente. Nomeado a coluna como Total Colaboradores 
16. Eliminar as colunas desnecessárias, que não serão usadas no relatório, de cada tabela ✅: Desabilitado carga de employee e mantido apenas funcionários com todas alterações solicitadas
Tabelas com as alterações solicitadas:

![image](https://github.com/Renatamoreirac/Dio-pbi/assets/147671867/523b00d9-7584-43f7-99af-174e5c8fcde4)

![image](https://github.com/Renatamoreirac/Dio-pbi/assets/147671867/e81241f0-560c-4595-9554-7f33120db1c2)



## Modelagem - Snowflake

![image](https://github.com/Renatamoreirac/Dio-pbi/assets/147671867/d676bb67-e942-4ea3-824f-8a7616e2cd77)


## Report para Caracterização dos dados

![image](https://github.com/Renatamoreirac/Dio-pbi/assets/147671867/180fca71-e91f-4b92-aa6c-a731905ed6bc)


