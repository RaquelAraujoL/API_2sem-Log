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
| **US06** | Média | Como Analista/Gestor eu quero que os nomes das cargas perigosas sejam padronizados, para que eu consiga filtrar e agrupar os tipos de produtos de forma precisa, sem variações ortográficas que separem o mesmo item.  | 3 | Concluido |
| **US07** | Média | Como Analista/Gestor, eu quero visualizar a Matriz Origem-Destino em um mapa interativo, para que eu possa identificar as rotas de cargas perigosas com maior fluxo e otimizar o planejamento de fiscalização regional.  | 5 | Concluido |
| **US08** | Média | Como Analista/Gestor, eu quero filtrar os dados por região, estado e tipo de carga, para que eu possa realizar análises granulares e entender o comportamento logístico de nichos específicos. | 3 | Concluido |
| **US09** | Média | Como Analista/Gestor, eu quero visualizar a evolução da movimentação através de gráficos de linhas ao longo dos anos, para que eu possa prever tendências de crescimento ou identificar quedas atípicas na movimentação de produtos perigosos. | 4 | Concluido |
| **US10** | Média | Como Analista/Gestor, eu quero identificar os modais mais utilizados (Rodoviário, Ferroviário, etc.) para cada categoria de carga perigosa, para que eu possa validar a adequação da infraestrutura utilizada e os riscos associados a cada modal.  | 5 | Concluido |

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





