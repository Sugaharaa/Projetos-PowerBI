# Projeto Power BI + Power Query – Azure Company Database  

Projeto prático desenvolvido como parte do bootcamp da [DIO](https://www.dio.me/), explorando **ETL com Power Query** e construção de um modelo relacional baseado no banco de dados **Azure Company**.  

---

## Objetivo  
O objetivo deste projeto foi trabalhar conceitos de **modelagem de dados** e **transformações no Power Query**, aplicando:  
- Mesclagem de consultas  
- Criação de colunas calculadas  
- Remoção e normalização de atributos  
- Agrupamentos e contagens  
- Criação de tabelas relacionais otimizadas para um **modelo estrela**  

---

## Scripts de Banco de Dados  

Os scripts originais para criação e inserção do banco **Azure Company** estão disponíveis nos links abaixo:  

- [Repositório completo da DIO](https://github.com/julianazanelatto/power_bi_analyst/tree/main/Módulo%203/Desafio%20de%20Projeto)  
- [Script de criação do banco](https://github.com/julianazanelatto/power_bi_analyst/blob/main/M%C3%B3dulo%203/Desafio%20de%20Projeto/script_bd_company.sql)  
- [Script de inserção de dados e queries](https://github.com/julianazanelatto/power_bi_analyst/blob/main/M%C3%B3dulo%203/Desafio%20de%20Projeto/insercao_de_dados_e_queries_sql.sql)  

---

## Etapas Realizadas no Power Query  

### 1. Conexão com o banco  
- Importação das tabelas `department`, `dept_locations`, `employee`, `dependent`, `project`, `works_on`.  

### 2. Transformações no Power Query  
- **Departament**: limpeza de colunas, normalização de nomes e datas.  
- **Dept_Locations**: expandir e mesclar com departamentos.  
- **Employee**:  
  - Mesclar colunas de nome em **FullName**  
  - Remover atributos redundantes (ex: endereço detalhado, minit, etc.)  
  - Criar versão final (`employee_Final`).  
- **Dependent**: relacionar dependentes com funcionários (`Essn`).  
- **Works_on**: normalizar participações de funcionários em projetos e horas trabalhadas.  
- **Project**: relacionar projetos com departamentos e works_on.  

### 3. Agregações  
- Contagem de subordinados por gerente (`SuperSsn_Count`).  

### 4. Estrutura Final  
Foram criadas tabelas refinadas e normalizadas para análise:  
- `azure_company_employee_Final`  
- `azure_company_department_location`  
- `azure_company_project`  
- `azure_company_works_on`  
- `azure_company_SuperSsn_Count`  

Essas tabelas estão prontas para compor um **modelo estrela** em futuros módulos.  

---

## Prints do Projeto  

As etapas foram documentadas com capturas de tela disponíveis na pasta [`/imagens`](./imagens).  

Exemplos:  
- Department  
  ![Department](./imagens/azure_company_departament.png)  

- Employee (Final)  
  ![Employee Final](./imagens/azure_company_employee_final.png)  

- Works On  
  ![Works On](./imagens/azure_company_works_on.png)  

- Project  
  ![Project](./imagens/azure_company_project.png)  

(Confira a pasta para visualizar todos os prints )  

---

## Aprendizados  
- Como trabalhar **joins e merges** no Power Query  
- Criação de campos calculados e normalização de atributos  
- Construção de **pipeline ETL** simples, mas funcional  
- Preparação de dados para **modelos dimensionais**  

---

## Repositório  
Neste repositório você encontra:  
- Arquivo `.pbix` com todas as etapas realizadas no **Power Query**  
- Prints das etapas (para validação visual)  
- Este README documentando o processo  

---

## Conclusão  
Esse projeto mostrou como é possível usar o **Power Query** para manipulação de dados de forma intuitiva e escalável. Ele é um passo inicial para avançar em **modelagem dimensional** e posteriormente criar **dashboards interativos** no Power BI.  
