
# 🚀 MVP 3 - ANÁLISE CRÍTICA E SUPORTE À DECISÃO

## 🎯 OBJETIVO DO MVP3

* **Problema que Resolve:** A necessidade de evoluir de visualizações básicas para uma governança de dados rígida, eliminando distorções metodológicas (como a mistura incorreta de quilos e litros) e consolidando dashboards limpos e interpretativos para suporte a decisões regulatórias estratégicas.
* **Hipótese a Validar:** Que a aplicação de regras estritas de filtragem física (densidade de cargas), eliminação de modais inconsistentes (Aéreo) e centralização de visuais (Sankey e Cards de Modais) reduzem drasticamente a margem de erro analítico e aceleram a formulação de políticas públicas de segurança ambiental.
* **Valor Entregue:** Um ecossistema de dados totalmente auditável (rastreável ao RAPP/IBAMA), livre de redundâncias sistêmicas, e estruturado especificamente para apontar gargalos logísticos estaduais de forma direta para tomadores de decisão.

---

## 📋 PRIORIDADES E USER STORIE

| Rank | Prioridades | User storie| Pontos | Status | Corrida |
| --- | --- | --- | --- | --- | --- |
| 11 | Baixa | Como Analista/Gestor, eu quero extrair relatórios baseados na análise de impacto dos dados, para que eu possa embasar decisões governamentais sobre segurança ambiental e investimentos em rodovias ou ferrovias. | 6 | ConUG | 3 |
| 12 | Baixa | Como Analista/Gestor, eu quero localizar os gargalos logísticos nos estados (áreas de alta retenção ou saturação), para que eu possa sugerir melhorias em pontos críticos da malha de transporte. | 4 | ConUG | 3 |

---

## 🧩 DESCRIÇÃO DAS ENTREGAS (APRIMORADAS PELA SPRINT 3)

### GOVERNANÇA E SANEAMENTO DE DADOS FINAL (ENGINE PYTHON)

* **Refatoração por Critério de Densidade:** Interrupção de conversões genéricas de massa para volume, implementando uma regra restritiva com o método **.isin()** para isolar unicamente registros declarados originalmente em unidades legítimas de volume (LITROS, L, METROS CÚBICOS, M3, M³).
* **Segundo Cruzamento Regional e Limpeza:** Realização de merge para identificar a Região Metropolitana de destino, utilizando o método **.drop(columns=['Município', 'Município_y'])** para eliminar colunas redundantes ou homônimas.
* **Tratamento de Fronteiras:** Aplicação de **.fillna('NÃO SE APLICA')** para municípios fora de Regiões Metropolitanas oficiais, eliminando lacunas nulas (NaN) e garantindo uma exibição elegante no Power BI.

### REESTRUTURAÇÃO E CONSOLIDAÇÃO DO FRONT-END (POWER BI)

* **Aba 'Fluxo de Carga por Origem-Destino':** Mudança de título para 'Fluxo de Carga por Origem-Destino' e fusão das antigas páginas 'SP-Nacional' e 'Nacional-SP' em um único painel interativo utilizando o gráfico Sankey. Inclui também um segmentador de ano para consultas históricas (2013-2025). O indicador de quantidade permanece fixado estritamente na unidade de Litros (L).
* **Aba 'Movimentação por Empresa':** Limpeza visual com a remoção completa dos cartões (cards) antigos, concentrando 100% do foco na tabela detalhada de dados corporativos e situação regulatória.
* **Aba 'Distribuição Modal':** Remoção completa do modal Aéreo devido a inconsistências detectadas na base bruta do RAPP/IBAMA. Substituição dos gráficos antigos por cards de comparação direta e intuitiva entre os volumes dos modais remanescentes.
* **Aba 'Evolução Anual' e 'Projeção de Tendência':** Manutenção dos indicadores de volume total ao longo dos anos. Realocação estratégica dos indicadores de controle corporativo (Empresas Ativas, Empresas Encerradas e Total de Empresas) para a página de Projeção de Tendência, concentrando análises comportamentais em uma única tela.

---

## 📊 CRITÉRIOS DE ACEITAÇÃO ATUALIZADOS

* **Segurança Estatística (Filtro Volumétrico):** O banco de dados final não pode conter registros cujas unidades originais fossem de massa (Kg, Toneladas) ou inválidas. Apenas dados isolados pelo método **.isin()** nas unidades L, LITROS, M3 e M³ são permitidos.
* **Consistência do Modelo de Dados:** O DataFrame exportado para o Power BI deve possuir colunas limpas, sem a presença de sufixos redundantes de cruzamento (como **_y**) e com substituição estrita de nulos por 'NÃO SE APLICA' via método **.fillna()**.
* **Consolidação de Telas (Sankey):** As análises de fluxo devem residir em uma única página unificada denominada 'Fluxo de Carga por Origem-Destino', controlada obrigatoriamente por um segmentador de ano dinâmico.
* **Confiabilidade da Matriz Modal:** O modal Aéreo deve ser completamente omitido do modelo e dos visuais do Power BI devido às suas inconsistências de origem no RAPP/IBAMA. O comparativo deve ser exibido por meio de cards informativos diretos.
* **Rastreabilidade Corporativa:** As métricas de contagem estatística de empresas (Ativas/Encerradas/Total) devem estar localizadas exclusivamente na tela de Projeção de Tendência, mantendo a aba de Evolução Anual focada em dados volumétricos estritos.
