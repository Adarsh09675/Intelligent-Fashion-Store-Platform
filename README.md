# 👗 Intelligent Fashion Store Platform

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![.NET Core](https://img.shields.io/badge/.NET%20Core-8.0-blue.svg)](https://dotnet.microsoft.com/download)
[![Angular](https://img.shields.io/badge/Angular-16-red.svg)](https://angular.io/)
[![Docker](https://img.shields.io/badge/Docker-Enabled-blue.svg)](https://www.docker.com/)

An advanced, full-stack E-commerce ecosystem built with **ASP.NET Core 8** and **Angular 16**. This platform provides a seamless fashion shopping experience with real-time updates, secure payments, and high-performance monitoring.

![Cover](Screenshots/Screen1.png)

## 🌟 Key Features

- **🛍️ Complete E-commerce Cycle**: From product discovery to secure checkout with Stripe integration.
- **🔐 Secure Authentication**: Identity-based authentication with JWT tokens and role-based access control.
- **❤️ Wishlist & Favorites**: Personalized shopping experience with real-time discount notifications via SignalR.
- **💬 Community Interaction**: Commenting system with likes/dislikes and product rating capabilities.
- **🚀 High Performance**: Distributed caching with Redis and optimized data access using Repository/Unit of Work patterns.
- **📊 Enterprise Monitoring**: Integrated Prometheus and Grafana for real-time health and performance metrics.
- **📜 Centralized Logging**: Full observability using the ELK stack (Elasticsearch, Logstash, Kibana).
- **🐋 Containerized Architecture**: Easy deployment and scaling using Docker and Docker Compose.

---

## 🛠️ Technology Stack

### Backend
- **ASP.NET Core 8 Web API** (Clean Architecture)
- **Entity Framework Core 8** (SQL Server)
- **Redis** (Distributed Caching)
- **SignalR** (Real-time Notifications)
- **AutoMapper** & **Serilog**
- **Stripe API** (Payment Processing)

### Frontend
- **Angular 16** with **Angular Material**
- **RxJS** & **State Management**
- **Responsive UI/UX**

### DevOps & Monitoring
- **Docker & Docker Compose**
- **Prometheus & Grafana**
- **Elasticsearch & Kibana**

---

## 🏗️ Architecture Overview

The project follows the **Clean Architecture** principles, ensuring a separation of concerns and maintainability:
1.  **Domain**: Core entities and business logic.
2.  **Application**: Application logic, DTOs, and interfaces.
3.  **Infrastructure**: Data persistence, external services (Redis, Cloudinary, Stripe).
4.  **WebAPI**: Entry point, Controllers, and Middleware.

---

## 🚀 Getting Started

### Prerequisites
- [.NET 8 SDK](https://dotnet.microsoft.com/download/dotnet/8.0)
- [Node.js & npm](https://nodejs.org/)
- [Docker Desktop](https://www.docker.com/products/docker-desktop)

### 1. Configuration
Create an `appsettings.json` in the `FashionClothesAndTrends.WebAPI` section. Use the template provided below:

<details>
<summary>View appsettings.json Template</summary>

```json
{
  "ConnectionStrings": {
    "DefaultDockerDbConnection": "Server=sql_server2022,1433;Database=FashionClothesAndTrendsDB;User Id=sa;Password=YourSecurePassword;MultipleActiveResultSets=true;TrustServerCertificate=True",
    "Redis": "redis:6379,password=YourSecurePassword,abortConnect=false"
  },
  "Token": {
    "Key": "YourVeryLongAndSecureSecretKey",
    "Issuer": "https://localhost:5001",
    "Audience": "https://localhost:5001"
  },
  "CloudinarySettings": {
    "CloudName": "your_cloud_name",
    "ApiKey": "your_api_key",
    "ApiSecret": "your_api_secret"
  },
  "StripeSettings": {
    "PublishableKey": "pk_test_...",
    "SecretKey": "sk_test_...",
    "WhSecret": "whsec_..."
  }
}
```
</details>

### 2. HTTPS Certificate (Docker)
For running with HTTPS inside Docker, generate a self-signed certificate:
```bash
openssl req -x509 -newkey rsa:2048 -keyout key.pem -out cert.pem -days 365 -nodes -subj '/CN=localhost'
openssl pkcs12 -export -out localhost.pfx -inkey key.pem -in cert.pem -password pass:YourPassword
```
Copy `localhost.pfx` to `FashionClothesAndTrends.WebAPI/certs`.

### 3. Run with Docker
```bash
# Build and run
docker-compose up --build
```

---

## 📸 Project Showcase

### Infrastructure & Schema
| Monitoring | Database Diagram |
| :---: | :---: |
| ![Docker](Screenshots/ScreenExampleDocker1.png) | ![DB](Screenshots/FashionClothesAndTrendsDB.png) |

### UI Gallery
<details>
<summary>Click to expand gallery</summary>

![Screen2](Screenshots/Screen2.png)
![Screen3](Screenshots/Screen3.png)
![Screen4](Screenshots/Screen4.png)
![Screen5](Screenshots/Screen5.png)
![Screen6](Screenshots/Screen6.png)
![Screen7](Screenshots/Screen7.png)
![Screen8](Screenshots/Screen8.png)
![Screen9](Screenshots/Screen9.png)
![Screen10](Screenshots/Screen10.png)
![Screen11](Screenshots/Screen11.png)
![Screen12](Screenshots/Screen12.png)
![Screen13](Screenshots/Screen13.png)
![Screen14](Screenshots/Screen14.png)
![Screen15](Screenshots/Screen15.png)
![Screen16](Screenshots/Screen16.png)
![Screen17](Screenshots/Screen17.png)
![Screen18](Screenshots/Screen18.png)
![Screen19](Screenshots/Screen19.png)
![Screen20](Screenshots/Screen20.png)
![Screen21](Screenshots/Screen21.png)
![Screen22](Screenshots/Screen22.png)
![Screen23](Screenshots/Screen23.png)
![Screen24](Screenshots/Screen24.png)
![Screen25](Screenshots/Screen25.png)
![Screen26](Screenshots/Screen26.png)
![Screen27](Screenshots/Screen27.png)
![Screen28](Screenshots/Screen28.png)
![Screen29](Screenshots/Screen29.png)
![Screen30](Screenshots/Screen30.png)
</details>

---

## 👤 Author

**Adarsh**
- GitHub: [@Adarsh09675](https://github.com/Adarsh09675)

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---
*Developed for a modern fashion experience.*
