# CareerPilot AI 🚀

**CareerPilot AI** is a full-stack **Smart Job Tracking and ATS Resume Analyzer** platform built with **Java 21, Spring Boot**, and a responsive **HTML5, CSS3, and Vanilla JavaScript** frontend. It empowers job seekers to extract text from PDF resumes, analyze ATS compatibility and keyword matching against job descriptions, compare resume versions, and manage job applications and interviews from a unified dashboard.

---

## ✨ Key Features
- **PDF Resume Extraction & Parsing:** Automatically extracts text from uploaded PDF resumes (`PdfTextExtractor.java`) and validates structural resume sections (`ResumeSectionChecker.java`).
- **ATS Score & Keyword Matching:** Analyzes resume quality (`ResumeQualityAnalyzer.java`), extracts technical and soft skills (`SkillExtractor.java`), and evaluates keyword alignment against target job descriptions (`AtsService.java`, `KeywordMatch.java`).
- **ATS Comparison & Leaderboard:** Compares multiple resume versions side-by-side (`ats-comparison.html`, `AtsComparison.java`) and tracks top-performing resume scores (`AtsLeaderboard.java`).
- **Resume & Scan History:** Stores uploaded resumes and historical ATS analysis reports (`resume-history.html`, `ats-history.html`).
- **Job Application & Interview Tracker:** Tracks job applications, status updates, recruiter reviews, and interview stages (`applications.html`, `interviews.html`, `ApplicationController.java`, `InterviewController.java`).
- **Analytics Dashboard & Authentication:** Displays real-time job search statistics (`DashboardController.java`, `DashboardStats.java`) with secure user registration and login (`AuthController.java`).

---

## 🛠️ Tech Stack
- **Backend:** Java 21, Spring Boot, Spring Web (REST API), Spring Data JPA, Maven
- **Frontend:** HTML5, CSS3 (Glassmorphism UI), Vanilla JavaScript (ES6+)
- **PDF & Text Processing:** Custom PDF text extraction, section validation, and skill/keyword analysis utilities
- **Tools & IDEs:** Spring Tools for Eclipse, Visual Studio Code (Live Server), Git, GitHub

---

## 📂 Project Architecture

```text
career-pilot-project/
├── careerpilot-backend/                          # Spring Boot REST API Backend
│   └── src/main/java/com/careerpilot/
│       ├── controller/                           # REST API Endpoints
│       │   ├── ApplicationController.java
│       │   ├── AtsController.java
│       │   ├── AuthController.java
│       │   ├── DashboardController.java
│       │   ├── InterviewController.java
│       │   ├── JobDescriptionController.java
│       │   └── ResumeController.java
│       ├── model/                                # JPA Entities & Request/Response DTOs
│       │   ├── Application.java, Interview.java, JobDescription.java, Resume.java, User.java
│       │   ├── AtsAnalysis.java, AtsComparison.java, AtsLeaderboard.java, AtsResult.java
│       │   ├── DashboardStats.java, KeywordMatch.java, RecruiterReview.java
│       │   └── Request/Response DTOs (AtsRequest, LoginRequest, PdfAtsRequest, PdfExtractRequest, etc.)
│       ├── repository/                           # Spring Data JPA Repositories
│       │   ├── ApplicationRepository.java, AtsAnalysisRepository.java, DashboardRepository.java
│       │   └── InterviewRepository.java, JobDescriptionRepository.java, ResumeRepository.java, UserRepository.java
│       ├── service/                              # Business Logic Layer
│       │   ├── ApplicationService.java, AtsService.java, AuthService.java, DashboardService.java
│       │   └── InterviewService.java, JobDescriptionService.java, ResumeService.java
│       ├── util/                                 # Core Resume & ATS Processing Utilities
│       │   ├── PdfTextExtractor.java
│       │   ├── ResumeQualityAnalyzer.java
│       │   ├── ResumeSectionChecker.java
│       │   └── SkillExtractor.java
│       └── CareerpilotAiApplication.java         # Spring Boot Main Entry Point
│
└── careerpilot-frontend/                         # Client-Side Web Application
    ├── assets/                                   # Images and static assets
    ├── css/                                      # Stylesheets (style.css, dashboard.css)
    ├── js/                                       # Modular Fetch API & UI logic (ats.js, dashboard.js, etc.)
    ├── login.html & register.html                # Authentication views
    ├── dashboard.html                            # Main analytics & overview dashboard
    ├── ats.html, ats-comparison.html, ats-history.html
    ├── resume-history.html                       # Saved resumes & versions
    └── applications.html & interviews.html       # Job & interview tracking views
```

---

## 🔌 Core REST API Modules

| Controller | Base Responsibility |
| :--- | :--- |
| `AuthController` | User registration, login authentication, and account access |
| `ResumeController` | Resume uploads, PDF text extraction, and resume version management |
| `JobDescriptionController` | Creating and managing target job descriptions |
| `AtsController` | Running ATS score evaluations, keyword matching, and resume comparisons |
| `ApplicationController` | Tracking job applications and application status updates |
| `InterviewController` | Scheduling and updating interview rounds and feedback |
| `DashboardController` | Aggregating career metrics and dashboard statistics |

---

## 🚀 Getting Started

### Prerequisites
- **Java Development Kit (JDK) 21** or higher
- **Maven 3.8+**
- **Relational Database** (configured in `application.properties`, e.g., MySQL)
- **Visual Studio Code** with the **Live Server** extension

### 1. Clone the Repository
```bash
git clone https://github.com
cd career-pilot-project
```

### 2. Run the Backend
1. Open `careerpilot-backend` in **Spring Tools for Eclipse**.
2. Open `src/main/resources/application.properties` and update your database URL, username, and password.
3. Right-click `CareerpilotAiApplication.java` and select **Run As > Spring Boot App** (starts on `http://localhost:8080`).

### 3. Run the Frontend
1. Open `careerpilot-frontend` in **Visual Studio Code**.
2. Right-click `login.html` and choose **Open with Live Server**.

---

## 👨‍💻 Author
**SK Mahaboob Subhani**  
GitHub: [@SKMAHABOOBSUBHANI-810](https://github.com)
