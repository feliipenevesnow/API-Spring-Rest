# 🎓 API Spring Rest - Gestão de Alunos

Esta API foi desenvolvida com o objetivo de aplicar conhecimentos avançados de **Spring Boot**, focando na criação de um serviço robusto de gerenciamento de alunos. O diferencial deste projeto é a integração com um serviço de consulta de CEP para preenchimento automático de endereços.

---

## 🚀 Tecnologias Utilizadas

* **Java 17+**: Linguagem base do ecossistema.
* **Spring Boot 3**: Framework para agilizar o desenvolvimento.
* **Spring Web**: Para criação dos endpoints RESTful.
* **Spring Data JPA**: Abstração de persistência de dados.
* **Jakarta Validation**: Garantia de integridade dos dados de entrada.
* **Maven**: Gerenciador de dependências.

---

## ✨ Funcionalidades Principais

* **CRUD Completo de Alunos**: Cadastro, listagem, consulta por matrícula, atualização total e remoção.
* **Integração de CEP**: Ao cadastrar um aluno, o sistema utiliza um `HttpClient` para buscar o endereço automaticamente baseado no CEP fornecido.
* **Atualização Parcial (Patch)**: Endpoint específico para atualização de CPF, demonstrando uso correto do método `PATCH`.
* **Tratamento de Respostas**: Uso de `ResponseEntity` para retornar códigos de status HTTP apropriados (200 OK, 201 Created, 404 Not Found).
* **Camada de DTO**: Utilização de `AlunoDTO` para isolar a regra de negócio da entrada de dados externa.

---

## 📂 Estrutura do Projeto

O projeto segue o padrão de camadas do Spring:

- `controller`: Porta de entrada da API (Endpoints).
- `service`: Concentra a lógica de negócio.
- `model`: Entidades mapeadas para o banco de dados.
- `dto`: Objetos de transferência de dados para requisições.
- `httpClient`: Lógica de consumo de APIs externas (Busca de CEP).
- `repository`: Interface de comunicação com o banco de dados.

---

## 🛠️ Endpoints Principais

| Método | Endpoint | Descrição |
| :--- | :--- | :--- |
| **POST** | `/api/inserir` | Cadastra um novo aluno (e busca o CEP). |
| **GET** | `/api/achar/todos` | Lista todos os alunos cadastrados. |
| **GET** | `/api/achar/{matricula}` | Busca um aluno específico por matrícula. |
| **PUT** | `/api/atualizar/{matricula}` | Atualiza todos os dados de um aluno. |
| **PATCH** | `/api/atualizar/{matricula}?cpf=...` | Atualiza apenas o CPF do aluno. |
| **DELETE** | `/api/deletar/{matricula}` | Remove um aluno do sistema. |

---

## 👨‍💻 Desenvolvedor

**Felipe Neves**
📍 Presidente Epitácio - SP
