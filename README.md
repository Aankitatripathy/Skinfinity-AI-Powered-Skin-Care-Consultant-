# Skinfinity – AI-Powered Skin Care Consultant  

Skinfinity is an academic system analysis and design project that envisions an AI‑powered skincare consultation platform. Instead of focusing on production code, it dives deep into how such a system should be specified, architected, secured, and delivered at scale.  

The work was completed as part of the **Advanced System Analysis & Design** course at the **University of South Florida – Muma College of Business**, with an emphasis on requirements engineering, user‑centric design, cloud‑based architecture, security, scalability, and Agile delivery practices.  

---

## Project Overview  

The modern skincare market is crowded with products, trends, and conflicting advice, making it hard for people to understand what actually works for their unique skin. Many users end up experimenting blindly, wasting money and sometimes harming their skin along the way.  

Skinfinity addresses this challenge by proposing an AI‑driven platform that combines facial image analysis with rich user input such as age, lifestyle, health history, and ingredient sensitivities to generate personalized skincare insights and recommendations. The system is designed as a secure, scalable, cloud‑native microservices architecture that supports AI analysis, user profiles, product recommendations, and dermatologist consultations, offering users a more informed, data‑driven path to healthier skin.  

---

## Objectives  

Skinfinity is designed with a clear focus on making skincare simpler, smarter, and more reliable for users. At a high level, the system aims to:  

- Reduce the trial-and-error approach in skincare by using AI-driven analysis of facial images and user data.  
- Deliver personalized, data-backed skincare recommendations tailored to each user’s skin type, lifestyle, and sensitivities.  
- Support scalable deployment through a cloud-based microservices architecture that can grow as usage increases.  
- Enforce strong security and privacy controls to protect sensitive information such as facial images and health-related details.  
- Provide an intuitive, mobile-friendly experience so users can access guidance seamlessly across devices.  

---

## Key System Features  

To support these objectives, Skinfinity brings together several core capabilities that work as one unified experience:  

- AI-based facial image analysis to detect concerns like acne, dryness, pigmentation, and redness.  
- Personalized product and routine recommendations generated from combined image analysis and questionnaire data.  
- User profiles and dynamic questionnaires to capture preferences, routines, allergies, and lifestyle factors.  
- Dermatologist consultation booking so users can easily schedule virtual expert sessions when needed.  
- Progress tracking over time, allowing users to compare before/after photos and monitor improvement trends.  
- Secure payment processing for premium services such as consultations or advanced recommendation features.  

---

## System Architecture  

Under the hood, Skinfinity is conceived as a microservices-based platform deployed on AWS, with each major function isolated into its own service and data store. This keeps the system modular, resilient, and easier to scale.  

**Core architectural elements include:**  

- An **API Gateway** that routes incoming requests from the frontend to the appropriate backend services.  
- Independent microservices for:  
  - User Profile Management  
  - Image Analysis  
  - Recommendation Engine  
  - Product Catalog  
  - Consultation Booking  
  - Payment Processing  
  - Progress Tracking  
  - Notifications & Feedback  
- Event-driven communication using technologies like **RabbitMQ** or **Kafka** for asynchronous workflows (e.g., “image processed” → “generate recommendations”, “payment completed” → “send confirmation”).  
- Serverless components (e.g., **AWS Lambda**) to handle background jobs such as scheduled reminders, batch processing, or non-blocking post-processing tasks.  

Together, these architectural choices support a system that is not only intelligent and personalized, but also robust, secure, and ready to scale as more users rely on it for their skincare journey.  

---

## Technology Stack (Proposed)  

Skinfinity is designed around a modern, cloud-native technology stack that aligns with its goals of scalability, performance, and secure handling of sensitive data. Each layer of the stack is chosen to play to its strengths, from AI workloads to a responsive user interface.  

**Core components:**  
- **Backend:** Java with Spring Boot for building modular microservices and RESTful APIs.  
- **AI / ML:** Python, using libraries like Scikit‑Learn and TensorFlow to power facial skin analysis and recommendation models.  
- **Frontend:** Angular with TypeScript to deliver a responsive, interactive, and mobile‑friendly web experience.  

**Data & Storage:**  
- **PostgreSQL (AWS RDS)** for structured data such as users, appointments, and transactions.  
- **MongoDB Atlas** for flexible, document‑based data like questionnaire responses and AI outputs.  
- **DynamoDB** (or similar NoSQL store) for fast product catalog lookups and metadata queries.  

**Cloud & DevOps:**  
- AWS services including **S3, ECS, Lambda, API Gateway, IAM** for deployment, storage, serverless processing, and identity management.  
- **RabbitMQ / Kafka** for messaging and event‑driven communication between microservices.  

**Security:**  
- **OAuth 2.0** and **JWT** for secure authentication and session handling.  
- **AES‑256 encryption** to protect sensitive data at rest and in transit.  
- **AWS IAM** to enforce fine‑grained access control across services and resources.  

---

## Security & Scalability  

Because Skinfinity handles facial images, health‑related details, and payments, the design emphasizes security and resilience from the ground up, not as an afterthought.  

**Security measures:**  
- End‑to‑end encryption for data both at rest and in transit, ensuring sensitive information is always protected.  
- Role‑based access control (RBAC) so only authorized users (e.g., dermatologists, admins) can access certain functions and data.  
- Web application firewall (AWS WAF) to defend against common web threats such as SQL injection, XSS, and DDoS attacks.  

**Scalability & reliability:**  
- Auto‑scaling and load balancing to handle fluctuations in load without degrading performance.  
- Containerization with Docker and orchestration via Kubernetes/ECS to support horizontal scaling of individual services.  
- A fault‑tolerant, highly available architecture where failures in one service do not bring down the entire system.  

---

## Agile Delivery Approach  

The project is structured around a Scrum‑based Agile process to allow for continuous refinement as the idea, design, and constraints evolve.  

**Process highlights:**  
- Scrum methodology with clearly defined roles and ceremonies.  
- 2‑week sprints to deliver incremental progress and incorporate feedback regularly.  
- Iterative prototyping to validate flows, UX decisions, and system behavior early and often.  
- Continuous feedback loops from users, peers, and domain experts to fine‑tune requirements and design.  

**Tools & focus areas:**  
- Tools: **JIRA** for backlog and sprint management, **GitHub** for collaboration and version control, and **Zoom** for distributed team communication.  
- Sprint themes included:  
  - Authentication and user onboarding  
  - AI‑driven skin analysis  
  - Recommendation logic and product mapping  
  - Performance, security, and reliability optimizations  

This approach keeps Skinfinity grounded in real user needs while ensuring that technical decisions can evolve alongside the design.  

---

## Notes  

This repository focuses on **system design and architectural planning** for the Skinfinity platform. It documents how the system should behave, how it should be structured, and which technologies and patterns it should use.  

There is **no production-ready application code or trained AI model** in this repo. Instead, it serves as a complete blueprint: requirements, architecture diagrams, UX flows, security and scalability strategies, and Agile project planning.  

---

## Team & Contributions  

Skinfinity was developed as a team project for the **Advanced System Analysis & Design** course. Each team member contributed across both technical and user-focused aspects of the work, including:  

- Gathering and analyzing requirements from users and stakeholders.  
- Designing the overall system architecture and microservices layout.  
- Planning security and scalability strategies for a cloud-native deployment.  
- Shaping the UX/UI, interaction flows, and accessibility considerations.  
- Producing detailed documentation, diagrams, and reflections on the design process.  

---

## Design & Prototype Links  

A major part of this project is the user-centric design work captured in Figma. These artifacts show how the idea evolved from rough flows to polished, interactive screens:  

**Low-Fidelity Wireframes**  
Early sketches of navigation, information hierarchy, and core user journeys:  
https://www.figma.com/design/jttruvRwnI6KY20s2IuT0U/Skinfinity--User-Centric-Design?node-id=0-1&p=f  

**High-Fidelity Designs**  
Finalized visuals with branding, color system, typography, and refined layouts:  
https://www.figma.com/design/jttruvRwnI6KY20s2IuT0U/Skinfinity--User-Centric-Design?node-id=1-2&p=f  

**Interactive High-Fidelity Prototype**  
Clickable prototype that simulates real usage, including flows like image upload, analysis, and booking:  
https://www.figma.com/proto/jttruvRwnI6KY20s2IuT0U/Skinfinity--User-Centric-Design?node-id=122-2&p=f&scaling=scale-down&content-scaling=fixed&page-id=1%3A2&starting-point-node-id=122%3A2  
