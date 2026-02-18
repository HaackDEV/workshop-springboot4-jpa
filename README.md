[LICENSE__BADGE]: https://img.shields.io/github/license/Fernanda-Kipper/Readme-Templates?style=for-the-badge
[JAVASCRIPT__BADGE]: https://img.shields.io/badge/Javascript-000?style=for-the-badge&logo=javascript
[TYPESCRIPT__BADGE]: https://img.shields.io/badge/typescript-D4FAFF?style=for-the-badge&logo=typescript
[EXPRESS__BADGE]: https://img.shields.io/badge/express-005CFE?style=for-the-badge&logo=express
[VUE__BADGE]: https://img.shields.io/badge/VueJS-fff?style=for-the-badge&logo=vue
[NEST__BADGE]: https://img.shields.io/badge/nest-7026b9?style=for-the-badge&logo=nest
[GRAPHQL__BADGE]: https://img.shields.io/badge/GraphQL-e10098?style=for-the-badge&logo=graphql
[JAVA_BADGE]:https://img.shields.io/badge/java-%23ED8B00.svg?style=for-the-badge&logo=openjdk&logoColor=white
[SPRING_BADGE]: https://img.shields.io/badge/spring-%236DB33F.svg?style=for-the-badge&logo=spring&logoColor=white
[MONGO_BADGE]:https://img.shields.io/badge/MongoDB-%234ea94b.svg?style=for-the-badge&logo=mongodb&logoColor=white
[AWS_BADGE]:https://img.shields.io/badge/AWS-%23FF9900.svg?style=for-the-badge&logo=amazon-aws&logoColor=white
[PYTHON_BADGE]:https://img.shields.io/badge/Python-3.11.9-blue?style=for-the-badge&logo=python&logoColor=lightskyblue
[PRS_BADGE]:https://img.shields.io/badge/PRs-welcome-green?style=for-the-badge


<h1 align="center" style="font-weight: bold;">E-Commerce Order Management System 💻</h1>

![license][LICENSE__BADGE]
![spring][SPRING_BADGE]
![java][JAVA_BADGE]


<details open="open">
<summary>Table of Contents</summary>

- [🚀 Getting started](#started)

- [📍 API Endpoints](#routes)

---

</details>

<p align="center">
  <b>This project is an e-commerce management system built with Spring Boot 4 and JPA/Hibernate. It demonstrates a professional layered architecture with design patterns and development best practices.</b>
</p>

---

<h2 id="started">🚀 Getting started</h2>


<h3>Prerequisites</h3>

- [Java Development Kit (JDK) 25](https://www.oracle.com/java/technologies/downloads/)
- [Maven 4.0.0+](https://maven.apache.org/download.cgi)


<h3>Cloning</h3>

To clone this repository, open your terminal and run:


```bash
git clone https://github.com/HaackDEV/spring-boot-ecommerce-system.git
```

<h3>Environment Variables</h3>

Use the `application.properties.example` as reference to create your configuration file `application.properties` with your H2 database configuration:



```properties
# DATASOURCE
spring.datasource.driverClassName=org.h2.Driver
spring.datasource.url=jdbc:h2:mem:testdb
spring.datasource.username={YOUR_USERNAME}
spring.datasource.password={YOUR_PASSWORD}

# H2 CLIENT
spring.h2.console.enabled=true
spring.h2.console.path=/h2-console

# JPA, SQL
spring.jpa.database-platform=org.hibernate.dialect.H2Dialect
spring.jpa.defer-datasource-initialization=true
spring.jpa.show-sql=true
spring.jpa.properties.hibernate.format_sql=true
```

<h3>Starting</h3>

How to start your project

```bash
mvn clean install
mvn spring-boot:run
``````

The application will be available at: `http://localhost:8080`

---

<h2 id="routes">📍 API Endpoints</h2>

The API provides the following RESTful endpoints:

| route | description |
|-------|-------------|
| <kbd>GET /users</kbd> | Retrieve all users |
| <kbd>GET /users/{id}</kbd> | Get user by ID |
| <kbd>POST /users</kbd> | Create new user |
| <kbd>PUT /users/{id}</kbd> | Update user |
| <kbd>DELETE /users/{id}</kbd> | Delete user |

Other resources follow the same pattern:
- `/products` - Product management
- `/orders` - Order management
- `/categories` - Category management

### Request and Response Examples:

<h3 id="get-user">GET /users</h3>

**RESPONSE:** `200 OK`
```json 
[
  {
    "id": 1,
    "name": "Maria Brown",
    "email": "maria@gmail.com",
    "phone": "988888888"
  },
  {
    "id": 2,
    "name": "Alex Green",
    "email": "alex@gmail.com",
    "phone": "977777777"
  }
]

```

<h3 id="get-users-id">GET /users/{id}</h3>

**RESPONSE:** `200 OK`
```json 
{
  "id": 1,
  "name": "Maria Brown",
  "email": "maria@gmail.com",
  "phone": "988888888"
}
```

<h3 id="post-users">POST /users</h3>

**REQUEST:**

```json 
{
  "name": "Bob Brown",
  "email": "bob@gmail.com",
  "phone": "913919414"
}
```

**RESPONSE:** `201 Created`
```json 
{
  "id": 3,
  "name": "Bob Brown",
  "email": "bob@gmail.com",
  "phone": "913919414",
  "password": null
}
```

<h3 id="put-users">PUT /users/{id}</h3>

**REQUEST:**

```json 
{
  "name": "John Doe Update",
  "email": "john.update@example.com",
  "phone": "977559955"
}
```

**RESPONSE:** `200 OK`
```json
{
  "id": 3,
  "name": "John Doe Update",
  "email": "john.update@example.com",
  "phone": "977559955"
}
```

<h3 id="delete-users">DELETE /users/{id}</h3>

**RESPONSE:** `204 No Content`

---
## License

---

This software is available under the following licenses:

- [MIT](https://rem.mit-license.org)