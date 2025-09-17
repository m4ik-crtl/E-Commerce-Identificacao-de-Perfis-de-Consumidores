# Projeto E-Commerce: Identificação de Perfis de Consumidores

## 📄 Descrição
Este projeto de ciência de dados realiza uma segmentação completa de clientes de uma empresa de e-commerce. A análise transforma dados transacionais brutos em perfis de consumidores acionáveis, utilizando tanto técnicas de negócio (RFM) quanto de Machine Learning (K-Means). O objetivo final é fornecer recomendações estratégicas para otimizar as ações de marketing e retenção.

---

## ✨ Links Importantes
- **[Dashboard Interativo no Tableau Public](https://public.tableau.com/views/Ecommerce-Dashboard_17576889597680/Ecommerce-Painel?:language=en-US&publish=yes&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)**
- **[Notebook Completo no Google Colab](https://colab.research.google.com/drive/1j8m_Bp00YdKAVmLL7tvH9OL2kT1Lmzye?usp=sharing)**
- **[Dataset Completo](https://docs.google.com/spreadsheets/d/1B9FZnNZt9rWR9D4emTTH3Uei_J45ZJDZvdqwpieDPwY/edit?usp=sharing)**

---

## 🎯 Objetivos
- Limpar e preparar um grande volume de dados transacionais.
- Criar segmentos de clientes utilizando a metodologia RFM (Recência, Frequência, Valor).
- Aplicar o algoritmo de clusterização K-Means para uma segmentação não supervisionada.
- Validar estatisticamente as diferenças de comportamento entre os segmentos.
- Desenvolver um plano de ação estratégico com base nos insights gerados.

---

## 🛠️ Tecnologias Utilizadas
- **Python**
- **Pandas:** Para manipulação e análise de dados.
- **Scikit-learn:** Para padronização dos dados (`StandardScaler`) e aplicação do K-Means (`KMeans`).
- **Matplotlib** & **Seaborn:** Para visualização de dados e análise dos segmentos.
- **Tableau:** Para a criação do dashboard interativo.

---

## 🔬 Metodologia em Etapas
1.  **Análise Exploratória e Limpeza:** Tratamento de dados ausentes (`CustomerID`), remoção de transações inválidas (quantidades negativas) e otimização de memória.
2.  **Segmentação RFM:**
    - Cálculo das métricas de Recência, Frequência e Valor para cada cliente.
    - Criação de scores de 1 a 5 para cada métrica usando quintis (`qcut`).
    - Definição de 7 segmentos de negócio com base nos scores (ex: "Campeões", "Em Risco").
3.  **Clusterização com K-Means:**
    - Utilização do **Método do Cotovelo (Elbow Method)** para determinar o número ideal de clusters (k=4).
    - Padronização das features RFM com `StandardScaler`.
    - Treinamento do modelo K-Means para agrupar os clientes.
4.  **Teste de Hipóteses:**
    - Aplicação do teste **ANOVA** para verificar se existia diferença estatística no ticket médio entre os 4 clusters.
    - Realização de **Testes-T post-hoc** para comparar os pares de clusters e identificar as diferenças específicas.

---

## 📊 Principais Conclusões e Plano de Ação
- A análise combinada de RFM e K-Means provou ser eficaz, com ambos os métodos gerando segmentos consistentes e valiosos.
- **Plano de Ação Sugerido:**
    - **Campeões e Leais:** Focar em programas de fidelidade e acesso antecipado a produtos.
    - **Promissores:** Incentivar a segunda compra com ofertas personalizadas e recomendações.
    - **Em Risco e Hibernando:** Criar campanhas de reativação com descontos agressivos para trazê-los de volta.
