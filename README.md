# 🚀 CI/CD Pipeline Project (Git → GitHub → Jenkins → Tomcat)

## 📌 Project Overview
This project demonstrates a complete **CI/CD (Continuous Integration and Continuous Deployment)** pipeline for a Java web application.

Whenever code is pushed to GitHub, the pipeline is automatically triggered to build and deploy the application without any manual intervention.

---

## 🎯 Objective
To automate the process of:
- Code integration
- Build generation
- Deployment to server

---

## 🛠️ Tools & Technologies Used
- Git
- GitHub
- Jenkins
- Apache Maven
- Apache Tomcat
- Linux (EC2 Instance)
- SSH
  
Developer → GitHub → Webhook → Jenkins → Maven Build → WAR File → SSH → Tomcat → Live Application


---

## 🔄 Working Process

1. Developer pushes code to GitHub repository  
2. GitHub webhook triggers Jenkins automatically  
3. Jenkins pulls the latest code  
4. Maven builds the project and generates a `.war` file  
5. Jenkins deploys the WAR file to Tomcat using SSH  
6. Tomcat hosts the application  
7. Application becomes live in browser  

---

## 📂 Project Structure

ci-cd-pipeline-demo/
│
├── pom.xml
├── .gitignore
└── webapp/
└── index.jsp

---


---

## ⚡ Jenkins Job Configuration

- Job Type: Freestyle Project  
- Source Code: GitHub Repository  
- Branch: main  
- Build Trigger: GitHub Hook Trigger  
- Build Step: Maven (`clean package`)  
- Post-Build Action: Send WAR file via SSH  

---

## 🔐 Webhook Configuration

- Payload URL:http://<JENKINS-IP>:8080/github-webhook/

  - Content Type: `application/json`
- Trigger: Push events

---

## 🌐 Deployment Details

- Target Server: Apache Tomcat  
- Deployment Path: `/webapps/`  
- Artifact: `target/*.war`  

---

## 📸 Screenshots
(Add your screenshots here)

- GitHub Repository
- Jenkins Dashboard
- Webhook Setup
- Build Success Output
- Tomcat Deployment
- Application Live Output

---

## ✅ Key Features
- Fully automated CI/CD pipeline  
- Zero manual deployment  
- Real-time build and deployment  
- Scalable and production-like setup  

---

## 📈 Benefits
- Faster development cycle  
- Reduced human errors  
- Continuous integration and delivery  
- Improved efficiency  

---

## 🚀 Future Improvements
- Add automated testing stage  
- Use Docker for containerization  
- Implement Kubernetes for orchestration  
- Add monitoring tools (Prometheus, Grafana)  

---

## 👨‍💻 Author
**Harshavardhan**  
BCA Student | Aspiring Cloud & DevOps Engineer  

