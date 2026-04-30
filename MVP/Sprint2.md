🎯**OBJETIVO DO MVP2** 

* <ins>**Problema identificado:</ins>**  Necessidade de maior precisão visual nas rotas de cargas e atualização periódica dos dados para garantir a consistência das análises estratégicas.
 
* <ins>**Melhoria validada:</ins>** Implementação de mapas interativos para visualização da Matriz Origem-Destino (OD) e filtros granulares para análise regional.
 
* <ins>**Valor entregue:</ins>** Dashboards com navegação intuitiva que permitem identificar tendências de movimentação e comparar o desempenho de diferentes modais de transporte. 

---

🧩 **DESCRIÇÃO DA SOLUÇÃO**

 **Principais entregas nesta etapa:** 

* <ins>**Mapa de Fluxo:</ins>** Implementação de visual de mapa para exibir a Matriz Origem-Destino das cargas perigosas.

* <ins>**Segmentação Avançada:</ins>** Filtros interativos por região, estado e tipo de produto.
   
* <ins>**Gráficos de Tendência:</ins>** Visualização da evolução da movimentação ao longo dos anos via gráficos de linhas.
  
* <ins>**Saneamento de Dados:</ins>** Padronização dos nomes das cargas e eliminação de duplicidades via Python 

 **Tecnologias utilizadas:** 
* Python (Google Colab)
* Pandas
* Power BI
* GitHub
* Excel

---

📋 **USER STORIES (SPRINT 2)** 

| ID | Prioridade | User Storie | Pontos | Status | Sprint |
| :--- | :--- | :--- | :--- | :--- | :--- |
| 6 | Média |  Como Analista/Gestor eu quero que os nomes das cargas perigosas sejam padronizados, para que eu consiga filtrar e agrupar os tipos de produtos de forma precisa, sem variações ortográficas que separem o mesmo item.  | 3 | Concluido | 2 |  |
| 7 | Média |  Como Analista/Gestor, eu quero visualizar a Matriz Origem-Destino em um mapa interativo, para que eu possa identificar as rotas de cargas perigosas com maior fluxo e otimizar o planejamento de fiscalização regional.  | 5 | Concluido | 2 |  |
| 8 | Média |  Como Analista/Gestor, eu quero filtrar os dados por região, estado e tipo de carga, para que eu possa realizar análises granulares e entender o comportamento logístico de nichos específicos.  | 3 | Concluido | 2 |  |
| 9 | Média | Como Analista/Gestor, eu quero visualizar a evolução da movimentação através de gráficos de linhas ao longo dos anos, para que eu possa prever tendências de crescimento ou identificar quedas atípicas na movimentação de produtos perigosos.  | 4 | Concluido | 2 |  |
| 10 | Media | Como Analista/Gestor, eu quero identificar os modais mais utilizados (Rodoviário, Ferroviário etc.) para cada categoria de carga perigosa, para que eu possa validar a adequação da infraestrutura utilizada e os riscos associados a cada modal.   | 5 | Concluido | 2 |  |

---

💡 **OBSERVAÇÕES** 

* <ins>**Foco da Etapa:</ins>** Transição do "Cérebro" Extrair, Transformar e Carregar (ETL) para a "Visualização".
  
* <ins>**Ferramentas:</ins>** Utilização de Power BI para a criação de matriz Origem-Destino (OD) e Python para refinamento continuo.
  
* <ins>**Diferencial Logístico:</ins>** Implementação de filtros avançados por Modal de Transporte e Tipo de Carga para visão granular no IBAMA.
  
* <ins>**Dados:</ins>** Base consolidada cobrindo o período de 2013 a 2025. 

---

## 📅 SPRINT RELACIONADA


| Sprint | Entregas principais | Status |
| :--- | :--- | :--- |
| 2 | Desenvolvimento do Dashboard (Mapa OD, Filtros e Tendências). | Concluido | 
| 3 | Publicação de relatórios revisados e controle de versão no GitHub. | Em andamento | 

---

📊 **CRITÉRIOS DE ACEITAÇÃO** 
* <ins>**Visual de Mapa:</ins>** O dashboard deve obrigatoriamente exibir um mapa funcional que conecte os pontos de Origem e Destino das cargas.
  
* <ins>**Precisão de Filtros:</ins>** Os filtros de Região, Estado e Modal devem responder instantaneamente.
   
* <ins>**Gráficos de Tendência:</ins>** Visualização clara da evolução anual (2013-2025).
   
* <ins>**Consistência de Dados:</ins>** O total de registros no Power BI deve ser idêntico à base limpa gerada em Python.
   
* <ins>**Navegação:</ins>** Interface intuitiva (encontrar nichos específicos com no máximo 3 cliques).

---

📈  **MÉTRICAS DE AVALIAÇÃO** 
* <ins>**Tempo de Resposta do Dashboard:</ins>** O tempo que o painel leva para filtrar e carregar os visuais após a seleção de um estado ou modal.
* <ins>**Taxa de Cobertura de Modais:</ins>** Percentual de registros que possuem o modal corretamente identificado e categorizado no dashboard.
* <ins>**Redução de Erros de Geolocalização:</ins>** Percentual de registros que possuem o modal corretamente identificado e categorizado no dashboard.
* <ins>**Nível de Granularidade (Nacional para Estadual sem perda de performance):</ins>** Capacidade do sistema de descer do nível Nacional para o nível Estadual sem perda de performance.
* <ins>**Feedback de Usabilidade dos usuários-alvo:</ins>** Avaliação dos usuários-alvo (Gestores e Analistas) sobre a facilidade de interpretar a Matriz OD. 

---

🚀 **PRÓXIMOS PASSOS (PARA A SPRINT 3)** 
* Iniciar a redação do Relatório Técnico Interpretativo com foco em suporte a políticas públicas. 
* Identificar as Top 10 Empresas movimentadoras e os pricipais gargalos logísticos por estado. 
* Preparar a documentação final do código para publicação no GitHub.
  
---

📂 Anexos / Evidências
