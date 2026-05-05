🚀 rslearn
Uma biblioteca de machine learning amigável para iniciantes que automatiza pré-processamento, treinamento e avaliação.

Licença Python Status Contribuições

✨ Por que rslearn?
⚡ Configuração mínima — sem configuração complexa
🤖 Pipeline automático (escalonamento, divisão, avaliação)
📊 Métricas integradas para regressão e classificação
🧠 Projetado para iniciantes aprenderem conceitos de ML
🧩 API limpa e simples inspirada no sklearn

Release & Changes
Versão : 1.0.7 - 1.0.6
Data de lançamento: 2026-05-03

🚀 Features
Latest (In Pipeline & linear_model):
Pipeline com método de análise embutido com suporte à classe de regularizações
Suporte à função evaluation() em todas as classes
Mais informações: CHANGELOG
Mais informações de parâmetros (em Pipeline): README
Mais informações de parâmetros (em linear_models): README
Leia as Doc Strings para informações extras sobre parâmetros

Fix
Problema de verificação de shape em linear_model
Problema no Auto Scaler

Changed
Licença MIT para GNU GPL v3
analysis() para evaluate() no Pipeline

🗄️ New File & Folders
Folder: Pipeline
File: Pipeline/_pipeline.py
Download Version Specific Module
Downloads - Module

📊 Linear Models
Regressão Linear (uma e múltiplas features)
Regressão Logística (binária e multiclasse)
Ridge Regression (Regularização L2)
Lasso Regression (Regularização L1)
Elastic Net (L1 + L2)

📏 Metrics
Erro Quadrático Médio (MSE)
Erro Absoluto Médio (MAE)
Raiz do Erro Quadrático Médio (RMSE)
R² Score
Acurácia (para classificação)
✔ Suporta tarefas de saída única e múltiplas saídas

🔧 Preprocessing
StandardScaler
MinMaxScaler

🧪 Model Selection
Train-Test Split

Suporta stratify para amostragem balanceada

⚙️ Optimization Details
Todos os modelos no rslearn são implementados usando Gradient Descent.

⚠️ Important:

O escalonamento de features é altamente recomendado para convergência estável e mais rápida.

Use:

StandardScaler (recomendado)
ou MinMaxScaler

🤖 Auto Standard Scaling (Linear, Logistic, Ridge, Lasso, ElasticNet)
os modelos incluem recurso de StandardScaler embutido no método fit():

scale=True # padrão
Aplica automaticamente o escalonamento de features internamente
Ajuda a prevenir instabilidade numérica

📁 Project Structure
rslearn/
│
├── linear_model/
│ ├── _linear_regression.py
│ ├── _logistic_regression.py
│ ├── _ridge.py
│ ├── _lasso.py
│ ├── _elastic_net.py
│
├── preprocessing/
│ ├── _scaler.py
│
├── metrics/
│ ├── _regression.py
│
├── model_selection/
│ ├── _split.py
│
└── README.md

📌 Cada módulo contém seu próprio README detalhado com exemplos de uso e explicações.

🛠️ Installation
cd rslearn
Install Usable Library (Stable - Latest)
pip install rslearn-ML
Download Version Specific Module
Downloads Older Library

Install dependencies
pip install -r requirements.txt

📌 Quick Example
from rslearn.linear_model import LinearRegression
from rslearn.preprocessing import StandardScaler
import numpy as np

X = np.array([10, 20, 30])
y = np.array([5, 10, 15])

scaler = StandardScaler()
X_scaled = scaler.fit_transform(X)

model = LinearRegression()
model.fit(X_scaled, y)

print(model.predict([40]))

📚 Documentation
Cada pasta inclui seu próprio README.md

Cobre:

Uso
Parâmetros
Exemplos
Funcionamento interno

🎯 Goals of this Project
Entender algoritmos de ML do zero
Construir uma API estilo sklearn
Criar componentes de ML reutilizáveis e modulares
Aprender design de sistemas de ML do mundo real
Testar sua própria habilidade

🧑‍💻 Author
Rustam Singh Bhadouriya / guilherme augusto / will

📜 License
Este projeto está licenciado sob a licença GNU GPL v3.
