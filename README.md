# 🎓 Online Assessment Portal

A production-grade Online Examination Portal built with **Spring Boot**, designed for conducting secure, timed, and auto-evaluated online assessments. Built as part of the AICTE OIBSIP Java Development Internship.

---

## ✨ Features

### Authentication & Security
- Student registration and login with **BCrypt** password encryption
- Role-based access control (**ADMIN** / **STUDENT**) via Spring Security
- Session management with remember-me functionality
- Change password support

### Exam Management (Admin)
- Create, edit, delete, publish/unpublish exams
- Set duration, passing percentage, start/end time
- Question bank management (MCQ with 4 options, marks, difficulty, topic)
- View all student results with search

### Examination Window (Student)
- **Professional exam UI** inspired by real assessment platforms
- Live countdown timer with page-refresh persistence
- Question palette with color-coded status (answered, not answered, marked for review, not visited)
- Auto-save answers via AJAX — no progress lost
- Mark for review and clear response
- **Anti-cheating**: tab switch detection, window blur monitoring, warning counter, auto-submit after max warnings

### Results & Analytics
- Instant result calculation: score, percentage, pass/fail
- Full result history for students
- Admin dashboard with statistics (total students, exams, pass rate, average scores)
- Interactive charts using Chart.js

### Export & Reports
- Export results as **CSV** or **PDF** (Admin)

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|-----------|
| Backend | Java 21, Spring Boot 3.2 |
| Security | Spring Security 6, BCrypt |
| Database | MySQL, Spring Data JPA, Hibernate |
| Frontend | Thymeleaf, Bootstrap 5, Chart.js |
| PDF Export | OpenPDF |
| Build | Maven |

---

## 📸 Screenshots

> Screenshots will be added in a future update.

---

## 🚀 Getting Started

### Prerequisites
- **Java 21+** installed ([Download](https://adoptium.net/))
- **Maven 3.8+** installed ([Download](https://maven.apache.org/download.cgi))
- **MySQL 8.0+** installed and running ([Download](https://dev.mysql.com/downloads/))

### Database Setup

1. Start MySQL server
2. The database `exam_portal_db` will be **auto-created** on first run (no manual SQL needed)

### Configuration

1. Open `src/main/resources/application.properties`
2. Replace `YOUR_MYSQL_PASSWORD` with your actual MySQL root password:
   ```properties
   spring.datasource.password=your_actual_password
   ```

### Run the Application

```bash
# Clone the repository
git clone https://github.com/awadheshkumar07087-cyber/internship.git
cd internship

# Build and run
mvn spring-boot:run
```

The application starts at **http://localhost:8080**

### Default Admin Login
| Field | Value |
|-------|-------|
| Email | `admin@examportal.com` |
| Password | `Admin@123` |

> ⚠️ Change the admin password after first login.

---

## 📁 Project Structure

```
src/main/java/com/examportal/
├── config/          → Security configuration, data seeding
├── controller/      → HTTP request handlers (Auth, Student, Admin, Exam)
├── entity/          → JPA entities (User, Exam, Question, ExamAttempt, StudentAnswer)
├── repository/      → Spring Data JPA repositories
├── security/        → Custom UserDetailsService
├── service/         → Business logic (UserService, ExamService)
└── exception/       → Global exception handling

src/main/resources/
├── static/css/      → Stylesheets (main + exam window)
├── static/js/       → JavaScript (exam engine + anti-cheat)
└── templates/       → Thymeleaf HTML templates
```

---

## 🔒 Security Features

- BCrypt password hashing
- CSRF protection
- Role-based URL authorization
- Session fixation protection
- Anti-cheating monitoring during exams

---

## 📄 License

This project is built for educational purposes as part of the AICTE OIBSIP Internship Program.

---

## 👤 Author

**Awadhesh Kumar**

- UID: `24BCS10638`
- GitHub: [@awadheshkumar07087-cyber](https://github.com/awadheshkumar07087-cyber)
