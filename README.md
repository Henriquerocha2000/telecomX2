# Telecom X – Parte 2: Prevendo Churn

---

## 📘 Resumo do Projeto
 Nesta segunda fase será desenvolvido um pipeline de modelos preditivos para antecipar quais clientes estão mais propesos a cancelar os serviços da empresa.

---

## 🧠 Etapas do Projeto

### 1. **Pré-processamento de Dados**

* Foi realizado a remoção da coluna `ID_Cliente`.
* Transformação de variáveis categóricas usando **One-Hot Encoding**.
* Tratamento de valores ausentes (remoção dos registros com `NaN`).
* Detecção de desbalanceamento da variável alvo `Cancelou`.

### 2. **Balanceamento com SMOTE**

* A técnica **SMOTE** foi aplicada para gerar dados sintéticos da classe minoritária clientes que cancelaram,

### 3. **Análise de Correlação**

* Matriz de correlação gerada para avaliar quais variáveis têm maior relação com a evasão.
* Identificação de variáveis como `Tempo de contrato` e `Total gasto` com forte relação com o churn.

### 4. **Divisão dos Dados**

* Os dados foram divididos em **conjuntos de treino e teste (70/30)** para avaliar os modelos com imparcialidade.

### 5. **Criação de Modelos Preditivos**

#### 🔹 Modelo 1: Regressão Logística

* **Requer normalização**: aplicada com `StandardScaler`.
* Justificativa: modelo linear, útil para interpretar pesos e identificar fatores com maior impacto.

#### 🔸 Modelo 2: Random Forest

* **Não requer normalização**.
* Justificativa: modelo robusto para dados tabulares e capaz de lidar com variáveis categóricas codificadas.
