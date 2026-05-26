# Hi there 👋 I'm Youna Park!

I’m a backend engineer who enjoys building services with a focus on **optimization** and **AI integration**.

<br />

## 🛠 Tech Stack

- **Languages**: Java, Python, SQL
- **Frameworks**: Spring Boot, Spring MVC, JPA
- **Databases**: MySQL, Redis
- **DevOps**: AWS (EC2, RDS, S3, ECS), Docker/Compose, GitHub Actions, Nginx
- **Testing**: Prometheus, Grafana, JUnit5, JMeter
- **AI Tools**: YOLOv5, GPT-3.5, koBERT

<br />

## 📫 Contact Me

- **Email**: yndbsk9372@gmail.com 
- **Blog**: [pyounani.tistory.com](https://pyounani.tistory.com)
- **Portfolio**: [Portfolio](https://drive.google.com/file/d/1Xp69KYVo2B9jx81ScZtvVVltGN2sXKhM/view?usp=sharing)

<br />

## 🚀 Main Projects

### 🎨 AI-based BGM Generation System 
Backend & Infrastructure | 2025.03 – 2025.10
- **Tech Stack**: Python 3.11, FastAPI, Celery, Redis, MongoDB, AWS S3, Docker
- **Key Contributions**:
  - Built an asynchronous AI inference pipeline using Celery + Redis to prevent API blocking caused by long-running AI inference tasks
  - Improved timeout and polling overhead issues by introducing a Redis Pub/Sub + SSE-based real-time event communication architecture
  - Optimized GPU memory usage and inference stability by designing an input-based dynamic model loading strategy for AI models

🔗 [GitHub Repository](https://github.com/pyounani/4co4co-backend)

<br />

### 📖 AI English Story Learning App 
Backend & Infrastructure Lead | 2024.03 – 2025.02
- **Tech Stack**: Java 17, Spring Boot 3.2, JPA, MySQL 8.1, AWS (EC2, RDS, S3), Nginx, Docker, JUnit5
- **Key Contributions**:
  - Identified HikariCP connection pool bottlenecks during load testing and improved TPS and latency through thread pool, connection pool, and timeout tuning
  - Discovered excessive queries caused by JPA relationship design through AOP-based observability and resolved them by redesigning the ERD structure
  - Improved email verification latency by converting synchronous email processing into an asynchronous architecture and optimized thread pool behavior using Mock SMTP-based load testing
  - Designed a custom RetryPolicy to selectively retry only specific email delivery exceptions instead of relying on generic exception-based retries
  - Solved DB-S3 consistency issues during transaction rollbacks by designing an event-driven compensation and batch cleanup architecture
  - Implemented social login and JWT-based authentication using Spring Security and OAuth2

🔗 [GitHub Repository](https://github.com/pyounani/StoryTeller-BE)

<br />

### ✍️ Study Recruitment Platform 
Operations & Backend | 2025.01 – 2025.03
- **Tech Stack**: Java 17, Spring Boot, JPA, MySQL, Redis, AWS ECS, GitHub Actions
- **Key Contributions**:
  - Optimized a popular-post ranking API by analyzing execution plans (EXPLAIN) and redesigning the ranking query into a 2-step DB ranking structure
  - Improved infrastructure management efficiency by migrating to a managed container environment using AWS ECS

🔗 [GitHub Repository](https://github.com/pyounani/StarHub-BE)


<br />

Thanks for visiting! 😊
