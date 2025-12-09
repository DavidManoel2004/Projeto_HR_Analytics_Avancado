\# 📊 Projeto de HR Analytics: Risco de Rotatividade e Fatores de Compensação



\## Introdução

Este projeto de \*\*Análise de Recursos Humanos (HR Analytics)\*\* utiliza dados da força de trabalho para identificar os principais \*drivers\* de Rotatividade (Turnover) e avaliar a correlação entre compensação, carga horária e satisfação no trabalho. O objetivo é fornecer \*insights\* acionáveis para a diretoria de RH, focando na retenção de talentos e na otimização da performance.



\## 🎯 Desafios de Negócio e Metodologia

O projeto foi guiado pelas seguintes questões de negócio:



1\.  \*\*Rotatividade (Turnover):\*\* Quais são os cargos e/ou departamentos com maior risco de saída?

2\.  \*\*Performance:\*\* Qual é a Média de Desempenho da força de trabalho e quais grupos a puxam para cima/baixo?

3\.  \*\*Compensação vs. Carga:\*\* Existe correlação entre Salário, Carga Horária (Horas Extras) e Satisfação no Trabalho?

4\.  \*\*Tenura:\*\* Qual é o impacto do Nível Hierárquico e Tempo de Empresa na retenção?



\## 🛠️ Metodologia e Processo (ETL)

O projeto seguiu uma metodologia estruturada:



1\.  \*\*Extração e Limpeza (Python/Pandas):\*\*

&nbsp;   \* Importação e validação inicial do \*dataset\* (verificação de duplicatas e dados ausentes).

&nbsp;   \* \*\*Tratamento de Outliers:\*\* Aplicação de correção de \*outliers\* na coluna de remuneração (`MonthlyRate`) para evitar distorções na análise salarial.

2\.  \*\*Modelagem de Dados (Power BI):\*\*

&nbsp;   \* O \*dataset\* foi desnormalizado em um \*\*Esquema Estrela\*\* composto por três tabelas:

&nbsp;       \* \*\*FATO\\\_Performance:\*\* Contém métricas e valores (Salário, Desempenho, Rotatividade).

&nbsp;       \* \*\*DIM\\\_Funcionários:\*\* Contém atributos estáticos (`JobRole`, `JobLevel`).

&nbsp;       \* \*\*DIM\\\_Comportamento:\*\* Contém as escalas de satisfação (`JobSatisfaction`, `WorkLifeBalance`).

3\.  \*\*Cálculos (DAX):\*\* Criação de medidas chave como `Taxa de Rotatividade`, `Média Salarial` e `Média de Desempenho`.



\## 📈 Insights Chave do Dashboard



O Dashboard completo (disponível no arquivo `.pbix`) revelou os seguintes \*insights\* acionáveis:



\### 1. Risco Extremo de Rotatividade (Turnover)

\* A \*\*Taxa de Rotatividade\*\* geral é de \*\*16,12%\*\*, mas a análise por cargo revela um ponto de crise:

\* \*\*O cargo de `Sales Representative` apresenta uma Taxa de Rotatividade alarmante, superior a 40%\*\*. Esta é a área que exige intervenção imediata.



\### 2. A Correlação Salário vs. Satisfação

\* O \*\*Gráfico de Dispersão\*\* (Média Salarial vs. Média Satisfação) mostrou que:

&nbsp;   \* \*\*Funcionários que fazem Horas Extras (`OverTime: Yes`)\*\* recebem salários mais altos, mas não demonstram aumento proporcional na satisfação.

&nbsp;   \* \*\*Conclusão:\*\* O dinheiro e o esforço extra não estão compensando o desgaste, o que pode ser um fator de risco para o aumento futuro do \*turnover\*.



\### 3. Análise de Performance e Tenura

\* A \*\*Média de Desempenho\*\* geral é de \*\*3,15\*\* (em uma escala de 1 a 4), indicando um bom resultado geral, mas que deve ser monitorado por departamento.

\* O \*\*Tempo de Empresa\*\* tem correlação visível com o Nível Hierárquico (`JobLevel`), sendo maior nos níveis mais altos, reforçando a importância dos planos de carreira e retenção de líderes.



\## 💻 Tecnologias Utilizadas



\* \*\*Linguagem:\*\* Python

\* \*\*Bibliotecas:\*\* Pandas (Limpeza e Tratamento de Dados)

\* \*\*Visualização e Modelagem:\*\* Power BI Desktop

\* \*\*Versionamento:\*\* Git \& GitHub



\## 🔗 Visualização

O relatório completo pode ser visualizado abrindo o arquivo `Projeto 4 PBI.pbix` (ou o nome que você salvou).

