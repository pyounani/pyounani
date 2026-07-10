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
- **Portfolio**: [URL](https://drive.google.com/file/d/1_VKZb5jo48lAJm3oYmXKNIMzR5rhlRJ2/view?usp=sharing)

<br />

## 🚀 Main Projects

### 🎨 AI-based BGM Generation System
Backend & Infrastructure | 2025.03 – 2025.10
- **Tech Stack**: Python 3.11, FastAPI, Celery, Redis, MongoDB, AWS EKS, S3, Docker, Vault, GitHub Actions
- **Key Contributions**:
  - Built an asynchronous inference pipeline with Celery + Redis to eliminate request blocking caused by long-running AI inference, serving 300+ users at a live exhibition
  - Diagnosed task loss caused by abnormal Worker termination (Celery prefetch re-queuing duplicate tasks) and resolved it with a late-ACK + DB-state-based idempotency guard, guaranteeing exactly-once inference calls
  - Replaced polling-based status checks with an SSE-based real-time notification architecture, tuning retry/keepalive/timeout values based on measured ~90s inference latency
  - Stabilized GPU VRAM usage from a peak of 97% to 55–70% on an 8GB GPU by designing a Phase-based sequential model load/evict pipeline for the emotion-analysis → music-generation inference flow
  - Isolated GPU inference workloads by splitting EKS T2/G4dn node groups and applying Taint/Toleration-based GPU pod scheduling

🔗 [GitHub Repository](https://github.com/pyounani/4co4co-backend)
<br />


### 📖 LLM-based Personalized Fairy Tale Platform
Backend & Infrastructure Lead | 2024.03 – 2024.10
- **Tech Stack**: Java 17, Spring Boot 3.2, JPA, Spring Security, MySQL, AWS (EC2, RDS, S3), Nginx, Docker, GitHub Actions, Prometheus, Grafana, JMeter
- **Key Contributions**:
  - Diagnosed an HikariCP connection pool bottleneck under JMeter load testing (RDS max_connections vs. undersized pool causing thread wait); derived optimal thread pool size via Little's Law and re-tuned pool size, reducing peak latency 438ms → 258ms
  - Identified an N+1 query issue via AOP-based query observability, caused by JPA forcing eager loading on the non-owning side of a bidirectional OneToOne relationship; resolved by redesigning to a unidirectional relationship with foreign key ownership reassigned, improving response time 726ms → 96ms
  - Converted synchronous email verification into an async architecture and designed a custom RetryPolicy that separates fatal exceptions (invalid address, format errors) from retryable ones (connection failure, rate limit) with exponential backoff; validated thread pool (14) and queue size (30) using a self-built Mock SMTP load test, cutting response time 4733ms → 17ms
  - Solved DB-S3 orphan file issues on transaction rollback by capturing delete targets via an AFTER_ROLLBACK event listener and batch-processing them through a daily scheduler with chunked deletion (1000/batch)
  - Built JWT dual-token (Access/Refresh) authentication with Spring Security and OAuth2 social login
  - Configured Blue-Green deployment via AWS CodeDeploy + ALB, later migrated to a single EC2 + Nginx port-switching setup to reduce infrastructure cost
  - Wrote 175 unit tests covering core business logic, achieving 80% line coverage

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
