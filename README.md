🔐 Projeto de Login Backend com Java e Spring Boot

Este projeto é uma API de autenticação e login desenvolvida com Java e Spring Boot.
O objetivo é implementar um sistema seguro de registro de usuários, login, e validação de tokens JWT, seguindo boas práticas de segurança e arquitetura de software.

🚀 Tecnologias Utilizadas

☕ Java 17+

🌱 Spring Boot

🧰 Spring Security

🧩 Spring Data JPA

🗄️ PostgreSQL

🔑 JWT (JSON Web Token)

📦 Maven

🧭 Springdoc / Swagger (opcional, para documentação da API)

⚙️ Funcionalidades

📝 Registro de usuários

🔐 Login e autenticação com JWT

🔄 Renovação de token (refresh token) (opcional)

🚫 Proteção de rotas com autorização baseada em roles/perfis

🔍 Validação de credenciais

🧩 Integração com banco de dados PostgreSQL

🧱 Estrutura do Projeto
src/
├── main/
│   ├── java/
│   │   └── com.vitordutra.login/
│   │       ├── controller/
│   │       ├── dto/
│   │       ├── model/
│   │       ├── repository/
│   │       ├── security/
│   │       └── service/
│   └── resources/
│       ├── application.properties
│       └── data.sql (opcional)
└── test/

⚙️ Configuração do Banco de Dados

No arquivo src/main/resources/application.properties, configure o PostgreSQL:

spring.datasource.url=jdbc:postgresql://localhost:5432/nomedobanco
spring.datasource.username=seu_usuario
spring.datasource.password=sua_senha
spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
spring.jpa.properties.hibernate.format_sql=true

🧩 Como Executar o Projeto

Clonar o repositório

git clone https://github.com/vitordutra/login-backend.git


Acessar o diretório

cd login-backend


Executar o projeto

mvn spring-boot:run


Acessar a aplicação

API: http://localhost:8080

Swagger (se configurado): http://localhost:8080/swagger-ui.html

🧾 Endpoints Principais
Método	Endpoint	Descrição
POST	/auth/register	Registra um novo usuário
POST	/auth/login	Faz login e retorna o token JWT
GET	/user/profile	Retorna os dados do usuário logado (requer token JWT)
🔑 Exemplo de Login (JSON)

Requisição:

POST /auth/login
{
  "username": "vitordutra",
  "password": "123456"
}


Resposta:

{
  "token": "eyJhbGciOiJIUzI1NiIsInR5..."
}

🧑‍💻 Autor

Vitor Dutra Docker
📧 vitordutra1125@gmail.com

🪪 Licença

Este projeto está sob a licença MIT — sinta-se à vontade para usar e modificar.

