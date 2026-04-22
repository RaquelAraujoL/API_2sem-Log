#  MVP 1 - Projeto Logística IBAMA (Cargas Especiais) 

##  Objetivo do MVP 
* **Problema que resolve:** A dificuldade de consolidar e limpar dados brutos do IBAMA (RAPP) sobre movimentação de cargas perigosas, garantindo uma base confiável para análise. 
* **Hipótese a validar:** Que o tratamento de dados via Python/Pandas elimina redundâncias e valores nulos, permitindo uma modelagem de dados eficiente para Business Intelligence. 
* **Valor entregue:** Base de dados higienizada e primeira carga de dados no Power BI para visualização da movimentação histórica. 

##  Descrição da Solução 
### Funcionalidades principais incluídas:
* Automação de extração, limpeza e padronização de dados do IBAMA (RAPP) via Python/Pandas no Google Colab. 
* Geração de base consolidada em CSV e scripts de carga para o Power BI. 
* Dashboards interativos com mapas de fluxo (Origem-Destino) e filtros por região, estado e tipo de carga especial. 

### Limitações conhecidas:
* A atualização dos dados depende da extração manual dos relatórios anuais do IBAMA. 
* O MVP foca em cargas perigosas e especiais registradas entre 2013 – 2025. 

### Escopo limitado:
* Foco em fornecer as primeiras análises de movimentação logística e validar a utilidade da ferramenta para gestores ambientais e analistas de logística. 

##  Personas / Usuários-Alvo
1. **Pessoa 1 – Gestor de Logística e Infraestrutura:** Precisa de relatórios rápidos e precisos sobre a movimentação de cargas especiais para tomar decisões sobre rotas, segurança e investimentos em transportes. 
2. **Persona 2 – Analista de Dados / Ambiental:** Precisa de bases de dados do IBAMA (RAPP) limpas e padronizadas para identificar gargalos logísticos e garantir o cumprimento das normas de transporte de cargas perigosas. 

##  Histórias de Usuário (Sprint 1) 

| Rank | Prioridades | História do Usuário | Pontos | Status | Corrida |
| :--- | :--- | :--- | :--- | :--- | :--- |
| 1 | Alta | Como Analista/Gestor, eu quero realizar a extração e o tratamento de valores nulos e duplicados dos dados do IBAMA com registro no RAPP, para que a base de dados do dashboard seja confiável e livre de redundâncias. | 9 | Concluido | 1 |
| 2 | Alta | Como Analista/Gestor, quero mapear as principais origens e destinos das mercadorias para negociar melhores rotas com armadores e transportadoras | 4  | Concluido |  |
| 3 | Alta | Como Analista/Gestor, quero identificar as empresas que movimentam cargas perigosas com declaração realizada para garantir o cumprimento das normas ambientais. | 4 | Concluido  | 1 |
| 4 | Alta | Como Analista/Gestor, quero visualizar os modais de transporte utilizados para avaliar a eficiência dos acessos terrestres e planejar expansões. | 3 | Concluido  | 1 |
| 5 | Alta | Como Analista/Gestor, quero acompanhar a evolução da movimentação ao longo do tempo através de gráficos históricos para embasar decisões estratégicas. | 3  | Concluido  | 1 |

##  Observações
* Todas as histórias têm prioridade Alta e foram concluídas durante o Sprint 1.
* **Ferramentas utilizadas:** Python para tratamento de dados e Power BI para visualização e análise. 
* O foco é fornecer suporte à formulação de políticas públicas de logística e segurança ambiental com dados de movimentação de cargas limpos e confiáveis.

## Sprint(s) Relacionadas 

| Corrida | Entregas principais | Status |
| :--- | :--- | :--- |
| 1 | Automação de extração e limpeza de dados do IBAMA (Python + Pandas). | Concluido |
| 2 | Integração com Power BI, criação da matriz Origem-Destino e filtros de modais. | Concluido |
| 3 | Elaboração do relatório técnico analítico e publicação da documentação no GitHub. | Concluido |

##  Critérios de Aceitação
* O MVP deve permitir que o usuário visualize e filtre os dados consolidados de movimentação de cargas (2013–2025). 
* O sistema deve disponibilizar o download da base de dados tratada e consolidada em formato CSV. 
* O dashboard deve apresentar obrigatoriamente o Mapa de Fluxo (Matriz Origem-Destino) e a segmentação por modais de transporte. 
* **Métricas coletadas:** tempo de processamento do script de limpeza, precisão na identificação de cargas perigosas e feedback dos gestores sobre a clareza dos indicadores. 

## Métricas de Validação 
* Nº de inconsistências (duplicados/nulos) removidas durante o processo de ETL. 
* Tempo de processamento para a geração da base consolidada. 
* Feedback qualitativo dos analistas sobre a confiabilidade da base inicial. 

##  Próximos Passos: MVP 2 (Sprint 2) 
* **Ajuste de Precisão nas Métricas:** Revisar as medidas DAX (Power BI) para garantir que as toneladas e volumes reflitam exatamente a base tratada, corrigindo casas decimais. 
* **Análise por Modal:** Iniciar o cruzamento de dados para identificar qual modal (Rodoviário, Ferroviário etc.) é predominante para cada categoria de carga perigosa. 
* **Testes de Usabilidade:** Realizar uma demonstração para os "Gestores de Logística" para validar se os filtros de região e estado atendem às necessidades de fiscalização. 
* **Documentação de ETL:** Começar a redigir o manual técnico explicando como o script Python limpa os dados, facilitando a manutenção futura no GitHub. 

- Link colabe limpeza de dados: https://colab.research.google.com/drive/1LAeYP5MkqIlomHgFZOUsjb7Vgtn842dm?usp=sharing
