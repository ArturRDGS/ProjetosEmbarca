# Sistema de Chamada Emergencial para Pacientes em Ambientes Hospitalares

O sistema proposto tem como objetivo otimizar a comunicação entre pacientes, acompanhantes e a equipe de enfermagem em ambientes hospitalares. Para isso, serão instalados pontos de chamada (botões de emergência) junto aos leitos, permitindo que os pacientes ou seus acompanhantes acionem rapidamente o atendimento em casos de emergência.


## **Instalação e Configuração do Servidor**

### **1. Clonar o Repositório**

```bash
git clone https://github.com/Embarcatech-Residencia-CAPEDII/Projetos
cd ./chamada-de-enfermagem/server
```

### **2. Criar o Ambiente Virtual**
```bash
python -m venv .venv
```

```bash
source .venv/bin/activate   # Linux/MacOS
```

```bash
.venv\Scripts\activate      #Windows
```

### **3. Instalar o Flask e dependências**
```bash
pip install Flask
pip install flask-mqtt
pip install flask-pymongo
pip install dotenv
pip install paho-mqtt
```
### **4. No arquivo .env coloque as credenciais para conexão com seu Banco de dados e do broker 
```
MONGO_URI = ''
MONGO_DATABASE = ''

BROKER_KEY = ''
BROKER_TOPIC = ''
BROKER_IP = ''
BROKER_PORT = ''
```

### **4. Abrir o Servidor 
```bash
cd ./chamada-de-enfermagem/server/Mqtt/
```
```bash
py main.py        #Windows
```
```bash
python main.py    #Linux
```

### **5. Realizar um teste
Em outro terminal execute o arquivo pub_test.py
```bash
py pub_test.py  #Linux
```
```bash
python pub_test.py  #Linux
```

