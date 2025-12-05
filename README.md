# Users Service - GastroReview

Microservicio REST con seguridad JWT para gestión de usuarios.

## 🚀 Tecnologías

- Java 21
- Spring Boot 3.3.3
- Spring Security + JWT
- Spring Data JPA
- PostgreSQL (Neon)
- Spring Cloud Netflix Eureka Client
- Maven

## 📦 Compilar

```bash
mvn clean package -DskipTests
```

## ▶️ Ejecutar Localmente

```bash
mvn spring-boot:run
```

## 🌐 Puerto

Este servicio corre en el puerto **8081**.

## 🔧 Configuración para Render

### Build Command
```
mvn clean package -DskipTests
```

### Start Command
```
java -jar target/*.jar
```

### Variables de Entorno
```
DATABASE_URL=jdbc:postgresql://ep-crimson-waterfall-a5g2m7gj.us-east-2.aws.neon.tech:5432/neondb?sslmode=require
DATABASE_USERNAME=neondb_owner
DATABASE_PASSWORD=npg_VkPsxdU17tEG
EUREKA_CLIENT_SERVICEURL_DEFAULTZONE=https://gastroreview-eureka.onrender.com/eureka/
JWT_SECRET=mySecretKeyForJWTTokenGenerationThatIsAtLeast256BitsLong
JAVA_OPTS=-Xmx512m -Xms256m
PORT=8081
```

## 🔐 Endpoints Principales

- `POST /api/auth/register` - Registrar usuario
- `POST /api/auth/login` - Login (devuelve JWT token)
- `GET /api/users` - Obtener usuarios
- `GET /api/users/{id}` - Obtener usuario por ID

## 📊 Base de Datos

Tablas gestionadas:
- `users`
- `user_profiles`

## 📝 Notas

- Requiere conexión a PostgreSQL (Neon)
- Implementa autenticación JWT
- Se registra automáticamente en Eureka

## 🔗 Enlaces

- [Spring Security](https://spring.io/projects/spring-security)
- [JWT](https://jwt.io/)
