🧠 **MVP 2 - VISUALIZAÇÃO E INTELIGÊNCIA DE FLUXO**

Documento de Escopo Técnico Reformulado (Padrão IPEM-SP) 

---

🎯 **OBJETIVO DO MVP2** 

* **Problema Identificado:** Necessidade de maior precisão visual nas rotas de cargas, adequação de formatos numéricos aos padrões técnicos do IPEM-SP, regionalização das análises territoriais e conformidade regulatória sobre o transporte de resíduos perigosos.


* **Melhoria Validada:** Implementação de mapas interativos para visualização da Matriz Origem-Destino (OD), criação de segmentações específicas de fluxo (SP ➔ BR e BR ➔ SP), agrupamento por Regiões Administrativas paulistas, legenda oficial de situação cadastral (RAPP/IBAMA) e gráficos progressivos por modal.


* **Valor Entregue:** Dashboards com navegação intuitiva (máximo 3 cliques) que permitem identificar tendências de movimentação, avaliar conformidade legal e comparar o desempenho volumétrico de diferentes modais de transporte de forma clara e direta.



---

🧩 **DESCRIÇÃO DA SOLUÇÃO (PRINCIPAIS ENTREGAS)** 

* **Mapa de Fluxo & Matriz OD Avançada:** Implementação de visual de mapa funcional para exibir a Matriz Origem-Destino das cargas perigosas, incluindo botões de segmentação de dados exclusivos para isolar os fluxos de exportação interestadual (Origem: SP ➔ Destino: BR) e importação interestadual (Origem: BR ➔ Destino: SP).


* **Saneamento e Formatação Numérica:** Padronização dos nomes das cargas, eliminação de duplicidades via Python (`drop_duplicates`) e alteração estrita do formato de exibição de Notação Científica para Número Inteiro com separador de milhar (ex: transformar 1,2E+05 em 120.000).


* **Regionalização e Inteligência Territorial:** Criação de tabela de relacionamento (De-Para) para agrupar e filtrar os municípios de São Paulo por suas respectivas Regiões Administrativas (RAs) oficiais (ex: Vale do Paraíba, Campinas, etc.).


* **Painel de Conformidade e Legenda RAPP/IBAMA:** Inserção de legenda explicativa contextualizada no BI detalhando os status de situação cadastral:


* **Ativo:** Regular e autorizado a emitir MTR.


* **Suspenso:** Interrompido por pendências ou penalidade.


* **Cancelado:** Extinto definitivamente.


* **Inativo:** Sem movimentação nos prazos legais.




* **Notas de Engenharia e Regulação:** Inclusão de nota técnica explicativa fixa e visível sobre a obrigatoriedade do Plano de Ação de Emergência (PAE) para o transporte rodoviário ou ferroviário de resíduos perigosos (Classe I).


* **Gráfico Progressivo de Modais:** Implementação de gráfico de barras progressivas (ou Gauge/Bullet Chart personalizado) comparando o volume total movimentado entre o modal Rodoviário vs. Ferroviário.



> 🛠️ **Tecnologias Utilizadas:** Python (Google Colab), Pandas, Power BI, GitHub e Excel.
> 
> 

---
📋 **USER STORIE ATUALIZADAS (SPRINT 2)**
| ID | Prioridade | User storie | Pontos | Status |
| --- | --- | --- | --- | --- |
| **US01** | Média | Como Analista/Gestor, eu quero que os nomes das cargas perigosas sejam padronizados, para que eu consiga filtrar e agrupar os produtos sem variações ortográficas. | 3 | Concluído |
| **US02** | Média | Como Analista/Gestor, eu quero visualizar a Matriz Origem-Destino em um mapa interativo, para identificar as rotas com maior fluxo e otimizar a fiscalização. | 5 | Concluído |
| **US03** | Média | Como Analista/Gestor, eu quero filtrar os dados por região, estado e tipo de carga, para realizar análises granulares de nichos específicos. | 3 | Concluído |
| **US04** | Média | Como Analista/Gestor, eu quero visualizar a evolução da movimentação através de gráficos de linhas ao longo dos anos (2013-2025), para prever tendências de crescimento. | 4 | Concluído |
| **US05** | Média | Como Analista/Gestor, eu quero identificar os modais mais utilizados para cada categoria de carga, para validar a adequação da infraestrutura utilizada. | 5 | Concluído |
| **US06** | Alta | Como Gestor do IPEM-SP, eu quero ver os volumes em Números Inteiros Formatados (sem notação científica), para que a leitura dos relatórios seja imediata e precisa. | 3 | A Fazer |
| **US07** | Alta | Como Analista, eu quero filtrar rapidamente os fluxos específicos SP➔BR e BR➔SP através de segmentações de dados, para monitorar o balanço de resíduos nas fronteiras. | 5 | A Fazer |
| **US08** | Média | Como Gestor Regional, eu quero visualizar os dados de SP agregados pelas suas Regiões Administrativas oficiais, para planejar fiscalizações regionais direcionadas. | 5 | A Fazer |
| **US09** | Média | Como Fiscal do IPEM, eu quero ter acesso a uma legenda clara dos status cadastrais do RAPP/IBAMA no painel, para identificar a regularidade das empresas de forma ágil. | 3 | A Fazer |
| **US10** | Alta | Como Auditor Ambiental, eu quero comparar o volume dos modais Rodoviário e Ferroviário através de um gráfico de barras progressivas, para avaliar a matriz de risco. | 5 | A Fazer |

---

📊 **CRITÉRIOS DE ACEITAÇÃO ATUALIZADOS** 

* **Formato Numérico Estrito:** Nenhum campo volumétrico ou de contagem de carga pode exibir formato em notação científica (E+). Todos os dados devem estar formatados como número inteiro com separadores de milhar.


* **Precisão de Filtros (Matriz OD):** Devem existir botões de segmentação dedicados que isolem e filtrem instantaneamente na tela as rotas SP ➔ BR e BR ➔ SP.


* **Hierarquia Territorial:** O painel deve permitir a filtragem e agrupamento de municípios paulistas através de suas respectivas Regiões Administrativas (RAs) oficiais.


* **Informativos e Legendas Obrigatórias:** O dashboard deve conter de forma estática e visível a nota explicativa sobre o Plano de Ação de Emergência (PAE) para cargas perigosas de Classe I e a legenda detalhada dos status do RAPP/IBAMA.


* **Gráfico Progressivo:** O comparativo volumétrico entre os modais Rodoviário e Ferroviário deve ser dinâmico e usar uma estrutura visual de progresso clara.


* **Navegação Rápida:** A interface deve ser intuitiva, permitindo que o gestor encontre qualquer informação de nicho específico com no máximo 3 cliques.



---

🚀 **PRÓXIMOS PASSOS (PARA A SPRINT 3)** 

1. Iniciar a redação do Relatório Técnico Interpretativo com foco em suporte a políticas públicas do IPEM-SP.


2. Identificar as Top 10 Empresas movimentadoras de resíduos e mapear os principais gargalos logísticos por estado.


3. Desenvolver os scripts/fórmulas em DAX e Power Query (M) necessários para suportar os novos filtros e a tabela de Regiões Administrativas.


4. Preparar e documentar o código final limpo e tratado para publicação e controle de versão no GitHub.

📂 **ANEXOS / EVIDÊNCIAS**
<td align="center"><video src="https://github.com/user-attachments/assets/5f10ed04-8aa6-4275-acea-46035c2d4bd5"></video></td>





