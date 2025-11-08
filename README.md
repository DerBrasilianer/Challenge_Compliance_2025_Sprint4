# Challenge Compliance & QA – Sprint 4

## 📌 Projeto: Gestão de Frotas – Mobile + Backend Java

**Grupo: LTAKN)**

* Enzo Prado Soddano, RM557937
* Vinicius Prates Altafini, RM 559183
* Lucas Resende Lima, RM556564

---

## ✅ Parte A — Testes Manuais (Azure Boards)

Nesta sprint foram criados **6 casos de teste manuais** conforme solicitação do professor:

* São **2 casos de teste por PBI**, totalizando 3 PBIs.
* Os casos foram registrados no **Azure Boards** seguindo o template oficial do professor.
* Todos os testes possuem: descrição, dados de entrada, dados de saída, critérios de aceite e passos detalhados para execução.

### 🧩 PBIs Utilizadas

| PBI                                  | Funcionalidade testada                       | Sprint onde foi implementada |
| ------------------------------------ | -------------------------------------------- | ---------------------------- |
| **Login**                            | Autenticação de usuários                     | Sprint 4                     |
| **Cadastro de Motos e Pátios**       | CRUD de motos e pátios                       | Sprint 3                     |
| **Visualização de Motos e Pátios**   | Listagem de dados com atualização automática | Sprint 3                     |

⚠️ **Aviso Importante**

> Alguns testes ficam registrados na *Sprint 3* porque a funcionalidade (login) foi feita posteriormente.
> Os testes de cadastro e visualização foram criados na *Sprint 4*, pois fazem parte do desenvolvimento atual.

📎 **Link de acesso ao Azure Boards**
[Página Summary](https://dev.azure.com/RM557937/Challenge_Compliance_2025_Sprint4)
[Página de Test Cases](https://dev.azure.com/RM557937/Challenge_Compliance_2025_Sprint4/_testManagement/all?showFilters=true)

---

## ✅ Parte B — Testes Automatizados (Postman)

Como o sistema possui backend com API REST e frontend mobile, **optamos por realizar a automação via Postman**, conforme permitido pelo enunciado.

> Foram criados **4 casos de testes automatizados** utilizando Collection + Environment no Postman.

### 📂 Estrutura do repositório

```
/postman
   ├── collection
   │      └── collection.json
   └── environment
          └── environment.json
README.md
```

### 🧪 Casos de teste automatizados criados

| Nº | Nome do Teste              | Método | Endpoint         |
| -- | -------------------------- | ------ | ---------------- |
| 1  | Login (autenticação admin) | GET    | `/api/motos`     |
| 2  | Criar Pátio (automação)    | POST   | `/api/patios`    |
| 3  | Criar Moto (automação)     | POST   | `/api/motos`     |
| 4  | Remover Moto (automação)   | DELETE | `/api/motos/:id` |

---

## 🔧 Variáveis utilizadas na *environment* do Postman

Essas variáveis permitem que os testes rodem automaticamente sem trocar valores manualmente.

| Variável         | Descrição                              | Exemplo de valor                                   |
| ---------------- | -------------------------------------- | -------------------------------------------------- |
| `baseUrl`        | URL da API no Render                   | `https://challenge-java-2025-sprint4.onrender.com` |
| `authUser`       | Usuário admin padrão para autenticação | `admin`                                            |
| `authPass`       | Senha do admin                         | `adminpass`                                        |
| `createdPatioId` | ID do pátio criado durante o teste     | gerado dinamicamente                               |
| `createdMotoId`  | ID da moto criada durante o teste      | gerado dinamicamente                               |

---

## 🚀 Variáveis dentro da Postman Collection

| Nome da Variável                           | Responsabilidade                                |
| ------------------------------------------ | ----------------------------------------------- |
| `Authorization` (Basic base64)             | Envio de credenciais nas requisições            |
| `X-CSRF-TOKEN` (se retornado pelo backend) | Usado somente quando necessário, senão ignorado |

---

## ▶️ Vídeo de Demonstração (execução dos testes automatizados)

**🎥 Link do vídeo:**

> *[Vídeo de Demonstração](https://youtu.be/s02bYJAzQJ0)*

O vídeo mostra:

* Execução da collection completa no Postman.
* Cada teste rodando automaticamente.
* Validação das respostas e armazenamento das variáveis na environment.

---

## ✅ Como rodar os testes automatizados

1. Abrir o Postman
2. Importar os arquivos da pasta `/postman` do repositório
3. Selecionar o **environment** `Sprint4-Compliance`
4. Clicar em **Run Collection**
5. Assistir os casos sendo executados automaticamente

---

## 📚 Tecnologias Utilizadas

| Área            | Tecnologia                  |
| --------------- | --------------------------- |
| Backend         | Java Spring Boot (Render)   |
| Frontend Mobile | React Native (Expo)         |
| Banco           | PostgreSQL                  |
| QA – Automação  | Postman + Collection Runner |
| QA – Gestão     | Azure Boards                |

---

## ✅ Entrega conforme requerimentos da disciplina

* [x] Testes manuais criados no Azure Boards (Parte A)
* [x] Testes automatizados no Postman (Parte B)
* [x] Branch padrão configurada como `develop`
* [x] Repositório público no GitHub
