# Bootcamp Santander - Ferramenta de Simulação Financeira

Este repositório contém a planilha de simulação financeira e recomendação de alocação automatizada em Fundos Imobiliários (FIIs) desenvolvida ao longo do módulo "Tabelas e Análises de Dados" do Bootcamp.

---

## 📊 Perguntas que a Ferramenta Responde
A ferramenta auxilia o planejamento financeiro respondendo às seguintes perguntas para o investidor:

### 1. Painel de Investimento Mensal
* **"Quanto investir por mês?"** -> O usuário pode definir o valor que poderá investir (Ex: R\$ 500,00).
* **"Por quantos anos?"** -> O tempo planejado de investimento para a simulação (Ex: 5 anos).
* **"Taxa de rendimento mensal?"** -> Exibe a taxa aplicada ao cálculo de juros compostos.
* **"Patrimônio acumulado?"** -> Mostra o montante final obtido ao término do período estipulado.
* **"Dividendos mensais?"** -> Calcula a estimativa de renda passiva mensal gerada por esse patrimônio acumulado.

---

## 🧮 Como o VF e o PROCV entram nos cálculos:

O dinamismo e a automação da planilha são sustentados por duas funções principais do Excel:

* **Função VF (Valor Futuro):** Ela realiza o cálculo analítico de juros compostos com aportes periódicos. A fórmula avalia o valor investido mensalmente, a taxa de rendimento configurada e o tempo em anos (multiplicado por 12 meses) para retornar o patrimônio acumulado final.
* **Função PROCV (Procura Vertical):** Para encontrar a distribuição exata dos fundos imobiliários, a planilha faz uma busca vertical na tabela de matriz de perfis. Ela utiliza uma **CHAVE combinada** (ex: `AGRESSIVO-PAPEL` ou `CONSERVADOR-TIJOLO`) para localizar a linha correspondente e extrair o percentual exato sugerido para aquele perfil.

---

## 🏷️ Intervalos Nomeados Criados
Foram criados intervalos nomeados para os parâmetros fundamentais do sistema:
* **`Salário`**: Célula que armazena a renda mensal do usuário para basear os cálculos.
* **`Rendimento_Carteira`**: Percentual padrão estimado para o retorno dos dividendos.
* **`Sugestao_Investimento`**: Cálculo automático do valor recomendado para investir.
* **`Matriz_Perfis`** (ou intervalo equivalente): Área da tabela contendo a relação de CHAVEs, Perfis e os respectivos percentuais de cada tipo de FII para a busca do PROCV.

---

## 📈 Percentuais de Cada Perfil e Origem dos Dados
A distribuição de ativos varia de acordo com a tolerância ao risco configurada na matriz da ferramenta:

### Conservador
Focado na máxima previsibilidade e menor volatilidade, priorizando fundos de recebíveis e ativos físicos consolidados.
* **Papel:** 30%
* **Tijolo:** 50%
* **Híbridos:** 10%
* **FOFs:** 10%
* **Desenvolvimento:** 0%
* **Hotelaria:** 0%

### Moderado
Busca um equilíbrio entre segurança e ganho de capital, inserindo sutilmente categorias de maior risco comercial.
* **Papel:** 32%
* **Tijolo:** 35%
* **Híbridos:** 8%
* **FOFs:** 5%
* **Desenvolvimento:** 10%
* **Hotelaria:** 10%

### Agressivo
Focado em potencializar os ganhos e a renda no longo prazo, aceitando maior volatilidade em troca de prêmios mais altos em setores de risco.
* **Papel:** 50%
* **Tijolo:** 10%
* **Híbridos:** 5%
* **FOFs:** 5%
* **Desenvolvimento:** 20%
* **Hotelaria:** 10%

### Origem dos dados:
* Os percentuais foram estabelecidos com base nas orientações metodológicas fornecidas pelo Expert durante o treinamento do Bootcamp, simulando carteiras reais de mercado.

---

## 🛠️ O que foi mudado em relação à ferramenta do Expert
* **Customização de Identidade Visual:** Toda a estrutura lógica, fórmulas robustas (VF, PROCV, concatenações de chaves) e as regras de negócio de alocação foram mantidas estritamente fiéis ao projeto do Expert para garantir a integridade dos cálculos, visto que este é a minha primeira planilha. A única alteração realizada foi a  **reestruturação da identidade visual e aplicação de um novo logotipo customizado**, adaptando a apresentação da ferramenta para o meu portfólio pessoal.

  ## 📸 Prints da ferramenta preenchida, com a simulação para o perfil **Conservador** e para o perfil **Agressivo**

  <img width="607" height="868" alt="image" src="https://github.com/user-attachments/assets/d498d573-9fe7-4ea9-a2b2-3dd50fc568bb" />

  <img width="576" height="869" alt="image" src="https://github.com/user-attachments/assets/7d04f7e5-bfe7-475e-846b-a623bfb61216" />

