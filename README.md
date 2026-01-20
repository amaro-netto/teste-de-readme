# InsightSent — Inteligência de Dados e Análise de Sentimentos


![Java](https://img.shields.io/badge/java-%23ED8B00.svg?style=for-the-badge&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/spring_boot-%236DB33F.svg?style=for-the-badge&logo=springboot&logoColor=white)
![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![FastAPI](https://img.shields.io/badge/FastAPI-005571?style=for-the-badge&logo=fastapi)
![Scikit-Learn](https://img.shields.io/badge/scikit_learn-%23F7931E.svg?style=for-the-badge&logo=scikit-learn&logoColor=white)
![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/numpy-%23013243.svg?style=for-the-badge&logo=numpy&logoColor=white)
![Uvicorn](https://img.shields.io/badge/Uvicorn-000000?style=for-the-badge&logo=uvicorn&logoColor=white)
![Hugging Face](https://img.shields.io/badge/HuggingFace-FFAE1A?style=for-the-badge&logo=huggingface&logoColor=black)
![Kaggle](https://img.shields.io/badge/Kaggle-20BEFF?style=for-the-badge&logo=kaggle&logoColor=white)
![Imbalanced-learn](https://img.shields.io/badge/Imbalanced--learn-005571?style=for-the-badge&logo=python&logoColor=white)
![Joblib](https://img.shields.io/badge/Joblib-005571?style=for-the-badge&logo=python&logoColor=white)
![NLTK](https://img.shields.io/badge/NLTK-154360?style=for-the-badge&logo=python&logoColor=white)
![SpaCy](https://img.shields.io/badge/SpaCy-09A3D5?style=for-the-badge&logo=spacy&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-11557C?style=for-the-badge&logoColor=white)
![Seaborn](https://img.shields.io/badge/Seaborn-2E6F95?style=for-the-badge&logoColor=white)
![Maven](https://img.shields.io/badge/Maven-%23C71A36.svg?style=for-the-badge&logo=apachemaven&logoColor=white)
![H2 Database](https://img.shields.io/badge/H2_Database-%23003B57.svg?style=for-the-badge&logo=h2&logoColor=white)
![PlantUML](https://img.shields.io/badge/PlantUML-%23f2f2f2.svg?style=for-the-badge&logo=plantuml&logoColor=black)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white)
![Oracle Cloud](https://img.shields.io/badge/Oracle_Cloud-F80000?style=for-the-badge&logo=oracle&logoColor=white)


![Java](https://img.shields.io/badge/Java-21-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-3.4.5-6DB33F?style=for-the-badge&logo=springboot&logoColor=white)
![Python](https://img.shields.io/badge/Python-3.11-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![FastAPI](https://img.shields.io/badge/FastAPI-005571?style=for-the-badge&logo=fastapi&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-15-316192?style=for-the-badge&logo=postgresql&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Scikit-Learn](https://img.shields.io/badge/scikit_learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)
![JWT](https://img.shields.io/badge/JWT-Security-000000?style=for-the-badge&logo=json-web-tokens&logoColor=white)

---

### **Índice**
- Descrição do Projeto
- Front-end
- Tecnologias Utilizadas
- Estrutura do Projeto
- Execução do Projeto
- Fluxogramas do Sistema
- Equipe

---

### 📝 **Descrição do Projeto**

O **InsightSent** é uma plataforma de inteligência de dados desenvolvida para transformar o caos de feedbacks não estruturados em decisões estratégicas. 

Em um cenário onde **80% dos feedbacks de clientes são ignorados** por incapacidade de processamento manual, o InsightSent atua como uma central de inteligência que processa textos em tempo real, identifica o idioma (Português/Espanhol) e classifica o sentimento com alta precisão.

### **Diferenciais**
* 🚀 **Performance:** Respostas em menos de 100ms.
* 🌍 **Multilíngue:** Detecção automática de **PT-BR** e **ES** (Espanhol).
* 📊 **Inteligência Visual:** Dashboard integrado para acompanhamento de métricas.
* 🔒 **Segurança:** Arquitetura protegida com autenticação via Token JWT.

---

## ⚙️ **Arquitetura da Solução**

O projeto adota uma arquitetura de **Microserviços Conteinerizados**, garantindo escalabilidade e isolamento de responsabilidades.

### **1. Backend (O Maestro)**
* **Tecnologia:** Java 21 + Spring Boot 3.4.5.
* **Função:** Orquestração de chamadas, gestão de segurança (Spring Security), validação de dados e comunicação com o banco.
* **Comunicação:** Utiliza **OpenFeign** para comunicação HTTP de baixa latência com o serviço de IA.

### **2. Data Science (O Cérebro)**
* **Tecnologia:** Python 3.11 + FastAPI + Uvicorn.
* **Modelo:** Pipeline de Machine Learning utilizando **TF-IDF Vectorizer** (para transformar texto em números) e **Regressão Logística** (para classificação).
* **Treinamento:** Modelo treinado com um dataset unificado de ~470.000 avaliações (Olist, B2W e Amazon Reviews).

### **3. Frontend (A Interface)**
* **Tecnologia:** Vanilla JavaScript (ES6+), HTML5 e CSS3.
* **Design:** Interface limpa, responsiva e focada na experiência do usuário (UX), comunicando-se via Fetch API com o Backend.

### **4. Infraestrutura de Dados**
* **Banco de Dados:** PostgreSQL 15 rodando em container Docker.
* **Persistência:** Armazena usuários, logs de auditoria e histórico completo das análises para geração de insights futuros.

---

## 📊 **Fluxo de Dados (Pipeline)**

```mermaid
sequenceDiagram
    participant User as 👤 Usuário
    participant Front as 💻 Frontend
    participant Java as ☕ Backend API (Java)
    participant AI as 🧠 IA Service (Python)
    participant DB as 🗄️ PostgreSQL

    User->>Front: Digita o texto e clica em "Analisar"
    Front->>Java: POST /analise (c/ Token JWT)
    Java->>Java: Valida Token & Permissões
    Java->>AI: Envia texto cru (OpenFeign)
    AI->>AI: Detecta Idioma (PT/ES)
    AI->>AI: Vetorização (TF-IDF) + Predição
    AI-->>Java: Retorna JSON {sentimento, score, idioma}
    Java->>DB: Salva log da análise (Persistência)
    Java-->>Front: Retorna Resultado Completo
    Front-->>User: Exibe Gráfico de Confiança e Cor
```

> [!NOTE]
> O código do front-end encontra-se em funcionamento e integrado ao backend. Documentação e melhorias visuais poderão ser adicionadas nas próximas iterações do projeto.


### ⚙️ **Tecnologias Utilizadas**
Seguindo a arquitetura de microserviços, adotaremos a seguinte stack:
  
**Backend:** 
* Java 17 + Spring Boot 3 - API /sentiment
* Spring Web (REST) - Endpoints
* Spring Security (JWT)
* Spring Validation
* Lombok
* OpenFeign (HTTP client → Python)
* H2 Database (em memória)
* JUnit + Mockito (testes)
* Swagger/OpenAPI (Documentação)

**Data Science:**
  * Python 3.10 
  * Pandas, NumPy, Scikit-learn  
  * Joblib (persistência de modelo)  
  * FastAPI + Uvicorn (servidor de predição) 
  * Datasets (Hugging Face) 
  * Huggingface Hub  
  * KaggleHub 
  * Imbalanced-learn (tratamento de dados desbalanceados) 
  * NLTK / SpaCy (pré-processamento de texto, se aplicável) 
  * Matplotlib / Seaborn (visualização de dados) 
  

**Infra/Dev:**
* Git / GitHub (Monorepo)
* Docker + Docker Compose
* GitHub Actions (CI/CD)
* PlantUML(fluxogramas)

**Build/Deploy:**
* Oracle Cloud (futuro) 

### 📁 **Estrutura do Projeto**
* `/backend` - Código fonte da API Java
* `/data` - Notebooks e scripts de treinamento do modelo
* `/docs` - Documentação e fluxogramas
  * `fluxoCadastro.png` — Fluxo de cadastro de usuário 
  * `fluxoLogin.png` — Fluxo de autenticação  
  * `fluxoAnalise.png` — Fluxo de análise de sentimento 
  * `INFO.TXT` — Informações complementares 
* `/frontend` — Interface web da aplicação
  * `index.html` — Página inicial
  * `README.md` — Documentação do front-end
  * `server.py` — Script de servidor local (opcional)
  * `/src`
    * `/assets`
      * `/css`
        - app.css
        - dashboard.css
        - login.css
        - style.css
      * `/js`
        - auth-guard.js
        - dashboard.js
        - layout.js
        - login.js
        - register.js
        - script.js
    * `/pages`
      - dashboard.html
      - register.html
      - sentiment.html

#### Visão Geral do Repositório
```
hackathon-sentimentapi-analytics
│
├── backend/                # API Java (Spring Boot)
│   ├── src/...
│   └── pom.xml
│
├── data/                   # Serviço de Machine Learning (Python)
│   ├── notebooks/          # Jupyter Notebooks
│   ├── model/              # Modelo treinado (.joblib)
│   ├── app.py              # FastAPI
│   └── requirements.txt    # Dependências Python
│
├── frontend/               # Interface Web
│   ├── index.html
│   ├── server.py
│   └── src/
│       ├── assets/
│       │   ├── css/        # Estilos
│       │   └── js/         # Scripts
│       └── pages/          # Páginas HTML
│
├── docs/                   # Documentação
│   └── fluxogramas/
│       ├── fluxoCadastro.png
│       ├── fluxoLogin.png
│       ├── fluxoAnalise.png
│       └── INFO.TXT
│
└── README.md               # Documentação principal do projeto
```
---
## Execução do Projeto

### Como Executar **(VSCODE)**

> [!IMPORTANT]
> o serviço Python **deve estar em execução antes** de iniciar o backend Java.


Este projeto é composto por dois serviços principais que devem ser executados separadamente:

- Serviço de Machine Learning (Python + FastAPI)
- API Backend (Java + Spring Boot)

> [!IMPORTANT]
> O backend Java depende do serviço Python estar em execução.

#### 🔹 Pré-requisitos

Certifique-se de ter instalado:

- Java 17+

- Maven 3.8+

- Python 3.10+

- Git

#### 🐍 1. Executando o Serviço de Machine Learning (Python)

Responsável por classificar o sentimento dos feedbacks.
```bash
cd data
```

Crie e ative um ambiente virtual (opcional, mas recomendado):
```bash
python -m venv venv
source venv/bin/activate   # Linux/Mac
venv\Scripts\activate      # Windows
```

Instale as dependências:
```bash
pip install -r requirements.txt
```

Execute a API FastAPI:
```bash
uvicorn app:app --reload
```

📍 O serviço estará disponível em:
👉 http://localhost:8000

📄 Documentação automática (Swagger):
👉 http://localhost:8000/docs


#### ☕ 2. Executando o Backend (Java + Spring Boot)

Responsável por expor a API REST e integrar com o serviço Python.
```bash
cd backend
```
Execute a aplicação:
```bash
mvn spring-boot:run

```
📍 A API estará disponível em:
👉 http://localhost:8080

📄 Documentação Swagger/OpenAPI:
👉 http://localhost:8080/swagger-ui.html

#### 🔁 Fluxo de Funcionamento

1. O cliente envia um feedback para a API Java

2. O backend chama o serviço Python via HTTP (OpenFeign)

3. O modelo de Machine Learning classifica o sentimento

4. O resultado é retornado e persistido no banco H2

#### 🛑 Encerrando a Aplicação

Para encerrar os serviços, utilize:
```bash
CTRL + C
```
em ambos os terminais (Python e Java).

## Como Executar **(Docker)**

O projeto foi desenhado para ser executado com um único comando, abstraindo a complexidade de configuração de ambientes.

### **Pré-requisitos**
* Docker e Docker Compose instalados.

### **Passo a Passo**

1.  **Clone o repositório:**
    ```bash
    git clone [https://github.com/amaro-netto/hackathon-sentimentapi-analytics.git](https://github.com/amaro-netto/hackathon-sentimentapi-analytics.git)
    cd hackathon-sentimentapi-analytics
    ```

2.  **Suba a aplicação (Build & Run):**
    ```bash
    docker-compose up --build -d
    ```
    *Isso irá compilar o Java, construir a imagem Python, subir o banco PostgreSQL e configurar a rede interna.*

3.  **Acesse o Sistema:**
    * **Frontend (Aplicação):** `http://localhost:80` (Login e Dashboard)
    * **API Java (Swagger):** `http://localhost:8080/swagger-ui.html`
    * **API Python (Docs):** `http://localhost:8000/docs`

---
### 📊 Fluxogramas do Sistema

Abaixo estão os fluxos principais da aplicação:

#### 🔐 Fluxo de Cadastro
Representa o processo de criação de um novo usuário no sistema. 

```mermaid
flowchart TD
A(["Início"]) --> B["Cliente envia requisição<br/>(Cadastro)"]
B --> C["Receber dados do usuário<br/>(nome, email, senha)"]
C --> D["Validar formato dos dados"]
D --> E{"Dados válidos?"}

E -- Sim --> F["Persistir usuário<br/>no banco de dados"]
F --> G["Gerar token JWT"]
G --> H["Retornar resposta JSON<br/>com token"]
H --> I["Usuário cadastrado<br/>com sucesso"]
I --> J(["Fim"])

E -- Não --> K["Retornar erro JSON<br/>(dados inválidos)"]
K --> J
```

#### 🔑 Fluxo de Login
Representa o processo de autenticação de um usuário no sistema. 

```mermaid
flowchart TD
A(["Início"]) --> B["Cliente envia requisição<br/>(Login)"]
B --> C["Receber credenciais<br/>(email, senha)"]
C --> D["Validar credenciais<br/>no banco"]
D --> E{"Credenciais corretas?"}

E -- Sim --> F["Gerar token JWT"]
F --> G["Retornar resposta JSON<br/>com token"]
G --> H["Usuário logado<br/>com sucesso"]
H --> I(["Fim"])

E -- Não --> J["Retornar erro JSON<br/>(login inválido)"]
J --> I
```

#### 💬 Fluxo de Análise de Sentimento
Representa o processo de classificação automática de feedbacks em positivo, negativo ou neutro.

```mermaid
flowchart TD
A(["Início"]) --> B["Cliente envia requisição<br/>(Análise de Sentimento)"]
B --> C["Receber texto de entrada<br/>+ token JWT"]
C --> D["Validar token JWT"]
D --> E{"Token válido?"}

E -- Sim --> F["Detectar idioma<br/>(Português ou Espanhol)"]
E -- Não --> G["Retornar erro JSON<br/>(token inválido)"]
G --> Z(["Fim"])

F --> H{"Idioma suportado?"}

H -- Sim --> I["Pré-processar texto<br/>(TF-IDF)"]
I --> J["Classificar sentimento<br/>(Regressão Logística)"]
J --> K["Gerar previsão<br/>+ probabilidade"]
K --> L["Retornar resposta JSON<br/>com resultado"]
L --> M["Resultado da Análise<br/>(Sentimento)"]
M --> Z

H -- Não --> N["Retornar um JSON<br/>(Aleatório)"]
N --> M
```
---

### 👥 **Equipe do Projeto**

<a href="https://github.com/alessandroapolinario" title="Alessandro Apolin"><img width="160" src="https://i.ibb.co/JWjKwMx9/Alessandro-Apolin-rio.png"/></a> <a href="https://github.com/amaro-netto" title="Amaro Netto"><img width="160" src="https://i.ibb.co/Gf4bW8GB/backend-java.png"/></a> <a href="https://github.com/brunorm86" title="Bruno Machado"><img width="160" src="https://i.ibb.co/cc3gb9dT/bruno.png"/></a> <a href="https://github.com/MicheleLescano" title="Michele Lescano"><img width="160" src="https://i.ibb.co/gbV6q2f2/michele.png"/></a> <a href="https://github.com/Rshinna" title="Rodrigo Franco"><img width="160" src="https://i.ibb.co/jZ9TJ416/rodrigo.png"/></a> 

