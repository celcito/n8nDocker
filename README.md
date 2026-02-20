# 🚀 n8n Docker Setup

![Docker](https://img.shields.io/badge/Docker-Ready-blue)
![n8n](https://img.shields.io/badge/n8n-Latest-orange)
![License](https://img.shields.io/badge/license-MIT-green)

Projeto para executar o **n8n** via Docker com persistência de dados, autenticação básica e configuração pronta para desenvolvimento local.

---

## 📦 O que essa configuração cria

- ✅ Persistência de dados
- 🔐 Login com usuário e senha (Basic Auth)
- 🌐 Porta padrão `5678`
- 🗂️ Volume persistente em `/data/n8n`

---

## 📁 Estrutura do Projeto
├── docker-compose.yml
└── data/
└── n8n/



---

## ⚙️ Permissão da Pasta (IMPORTANTE)

Antes de subir o container, garanta permissão de leitura e escrita na pasta:

```bash
mkdir -p data/n8n
sudo chown -R 1000:1000 data/n8n
sudo chmod -R 755 data/n8n

## ⚙️ Verificar logs:


docker logs -f n8n


## ▶️ 4️⃣ Subir o container

Execute:

```bash
docker compose up -d


🌍 5️⃣ Acessar no navegador

Abra:

http://localhost:5678
🔐 Login padrão
user: admin
senha: admin123
