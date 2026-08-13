# 🎓 ISIMM University Portal — Web Project

**ISIMM Portal** is a web application created for **ISIMM University**, designed to provide information for general users and offer administrative and student functionalities through a hidden, secure interface.  

The project demonstrates **Spring Boot**, **MySQL**, and **Spring Security** integration, while showcasing creative access methods inspired by the **Konami Code** 🎮.

---

## 🏠 Home Page

The **home page** contains general information about ISIMM and is accessible to all users.  

Hidden access to the **admin** and **student** pages is enabled via special keyword entries:

- **Admin Page:** Type `admin` anywhere on the home page  
- **Student Page:** Type `etudiant` anywhere on the home page  

💡 This method is inspired by the Konami Code to **hide sensitive pages** from normal users instead of exposing them through buttons or menus.  

---

## 🔐 Access Control

### Admin Access
- After typing `admin`, a **login page** appears.  
- **Valid admin credentials** grant access to the **admin dashboard**.  
- Logging in with a **student account** triggers a **custom 403 error page**.

### Student Access
- After typing `etudiant`, students can log in to access their **personal dashboard**.

---

## 🛠️ Admin Functionalities

The admin can manage multiple aspects of the portal:

### 👩‍🎓 Student Management
- Add, edit, delete students  
- View the full list of students  
- Search for a student  
- Add student **marks** and **timetables**

### 🧑‍💻 Account Management
- Create, edit, or delete student accounts  
- View all accounts  

> Passwords are encrypted using **Spring Security**, so the admin cannot see student passwords.  
> Students can request a password reset from the admin if needed.

### 📰 News & Notifications
- Add, edit, delete news items  
- Check the news list  
- View notifications sent by users through the **“Contact Us”** form  

---

## 🧑‍🎓 Student Functionalities

Students can:  
- View profile information  
- Check their timetable  
- Review their marks  
- Access news and updates

---

## ⚙️ Setup & Running the Project

1. **Install dependencies:**  
   - MySQL  
   - Spring Boot (Java 17+)  
   > Optional: WAMP Server if MySQL setup is problematic  

2. **Configure database:**  
   - Edit `application.properties` with your MySQL username and password  
   - Create database `isimm_db`  

3. **Add Admin account manually:**  
   - Table `account`: add CIN, username, password  
   - Table `role`: add CIN, username, role (`ROLE_ADMIN`)  

4. **Run the application:**  
   - Launch as a Spring Boot app  
   - Open in browser: `http://localhost:8090/home`  

5. **Using the Admin dashboard:**  
   - Adding timetables or marks currently works for **“Ingenieur Informatique 1”**  
   - Comments in code explain how to extend functionality for other grades  

---

## 💡 Notes & Tips

- The **hidden login method** ensures normal users cannot access sensitive pages  
- Student accounts must be **created manually by the admin** for security  
- Spring Security ensures **encrypted passwords** and safe authentication  
- Timetables and marks can be expanded to other grades following the instructions in the code  

---

## 🎨 Tech Stack

- **Backend:** Spring Boot  
- **Frontend:** HTML, CSS, JavaScript  
- **Database:** MySQL  
- **Security:** Spring Security  

---

## 🚀 Credits

- Developed by **Nadine Mlayeh** for **ISIMM University Project**  
- Demonstrates secure access, student/admin management, and dynamic content

---

⭐ Enjoy exploring the ISIMM Portal! Remember: sensitive pages are hidden, so try the Konami-inspired code carefully 😉
