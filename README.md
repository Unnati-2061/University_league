#  University League (Delhi-NCR Higher Education Portal)

**University League** is a high-performance, production-ready educational aggregator and directory platform built for the Delhi-NCR market. The application catalogs detailed academic tracks, multi-tier fee structures, placement statistics, and user reviews for over 25+ premier regional institutions. 

This platform is engineered using **Java Spring Boot**, backed by a **live, highly available Cloud MySQL cluster**, and rendered using an SEO-optimized frontend engine to guarantee rapid search indexation for search engine crawlers.

---

##  Architecture & Tech Stack

The application follows a clean, decoupled N-tier MVC architecture:

* **Backend Engine:** Java / Spring Boot 3.x
* **Data Access & ORM:** Spring Data JPA / Hibernate
* **Database Infrastructure:** Managed MySQL Cluster (Hosted on Aiven Cloud, 24/7 Availability)
* **Optimization Tools:** Project Lombok (Boilerplate Elimination)
* **Frontend UI Engine:** Thymeleaf Template Engine + Bootstrap 5 (Server-Side Rendered for SEO)

---

## 💡 Key Features

* **Cloud-First Persistent Infrastructure:** Database schema normalized across 6 relational tables (`regions`, `universities`, `courses`, `fees`, `placements`, `reviews`) handling secure remote SSL-enforced handshakes.
* **Granular Academic Search Matrix:** Tracks and indexes granular academic programs spanning Undergraduate, Postgraduate, Integrated, and Doctoral paths along with sliding tuition fee attributes.
* **Commercial Filtering Pipeline:** Optimized repository queries allowing instantaneous user filtering by geographical sub-markets (Noida, Greater Noida, Delhi, Haryana NCR) and placement benchmarks (LPA packages).
* **SEO & Indexation Focus:** Leveraged Server-Side Rendering (SSR) via Thymeleaf to deliver pre-rendered, crawlable HTML files directly to Googlebot/Bingbot, solving standard client-side React single-page application indexation hurdles.

---

## 📁 Directory Structure

```text
com.collegedirectory.api/
│
├── entity/          # JPA Models mapping directly to Cloud SQL Tables
│   ├── Region.java
│   ├── University.java
│   └── Course.java
│
├── repository/      # Data Access Interfaces extending JpaRepository
│   ├── UniversityRepository.java
│   └── CourseRepository.java
│
├── service/         # Centralized Business & Filtering Core Logic
│   └── DirectoryService.java
│
└── controller/      # REST API Web Endpoints & UI Template Routers
    ├── UniversityController.java
    └── CourseController.java
