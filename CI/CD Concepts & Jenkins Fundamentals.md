### **🗓 Day 4: CI/CD Concepts & Jenkins Fundamentals**  

#### **🔹 Goals for the Day:**  
✅ Understand CI/CD concepts and its importance in DevOps  
✅ Learn Jenkins fundamentals and installation  
✅ Set up a basic CI/CD pipeline with Jenkins  
✅ Automate builds and deployments  

---

## **📌 Part 1: Understanding CI/CD (2 Hours)**  
🔹 **Topics to Cover:**  
- What is CI/CD? Why is it important in DevOps?  
- Continuous Integration (CI) vs Continuous Delivery (CD) vs Continuous Deployment  
- CI/CD Best Practices  
- Tools used in CI/CD (Jenkins, GitHub Actions, GitLab CI/CD, ArgoCD, Tekton, Spinnaker)  
- CI/CD Workflow in a DevOps pipeline  

🔗 **Resources:**  
- [What is CI/CD?](https://www.redhat.com/en/topics/devops/what-is-ci-cd)  
- [CI/CD Pipeline Explained](https://www.atlassian.com/continuous-delivery)  

💻 **Hands-on Exercise:**  
1. Draw a simple CI/CD workflow diagram for an application (e.g., Code -> Build -> Test -> Deploy).  
2. Research and compare Jenkins with other CI/CD tools.  

---

## **📌 Part 2: Jenkins Installation & Setup (2 Hours)**  
🔹 **Topics to Cover:**  
- Introduction to Jenkins: What is it and why is it used?  
- Installing Jenkins on Linux (Ubuntu/Debian or CentOS)  
- Installing Jenkins on Docker (`docker run -p 8080:8080 jenkins/jenkins:lts`)  
- Initial Jenkins setup and unlocking Jenkins  
- Installing necessary plugins  

🔗 **Resources:**  
- [Jenkins Installation Guide](https://www.jenkins.io/doc/book/installing/)  
- [Jenkins Docker Setup](https://hub.docker.com/r/jenkins/jenkins)  

💻 **Hands-on Exercise:**  
1. Install Jenkins on your local system or a cloud instance.  
2. Start Jenkins and unlock it using the administrator password.  
3. Install the recommended plugins and create your first admin user.  

---

## **📌 Part 3: Understanding Jenkins Jobs & Pipelines (2 Hours)**  
🔹 **Topics to Cover:**  
- Types of Jenkins Jobs (Freestyle, Pipeline, Multibranch, etc.)  
- Configuring and running a Freestyle job  
- Setting up Jenkins with GitHub (SSH key setup for Git)  
- Jenkins Pipeline as Code (Declarative vs Scripted Pipelines)  

🔗 **Resources:**  
- [Jenkins Pipeline Documentation](https://www.jenkins.io/doc/book/pipeline/)  

💻 **Hands-on Exercise:**  
1. Create a new **Freestyle Job** in Jenkins that pulls a GitHub repo and runs a shell script.  
2. Write a basic **Jenkinsfile** (Declarative pipeline) and run it.  

---

## **📌 Part 4: Building a CI/CD Pipeline with Jenkins (3 Hours)**  
🔹 **Topics to Cover:**  
- Using Jenkinsfile for CI/CD pipeline  
- Automating builds with Jenkins  
- Integrating Jenkins with Docker for containerized builds  
- Deploying applications using Jenkins  

🔗 **Resources:**  
- [Jenkinsfile Tutorial](https://www.jenkins.io/doc/book/pipeline/syntax/)  

💻 **Hands-on Exercise:**  
1. Write a Jenkins pipeline to:  
   - Clone a GitHub repository  
   - Build a Docker image  
   - Push it to Docker Hub  
   - Deploy to a Kubernetes cluster (if available)  
2. Trigger Jenkins builds automatically with GitHub Webhooks.  

---

## **📌 Part 5: Jenkins Integration with Tools (1 Hour)**  
🔹 **Topics to Cover:**  
- Integrating Jenkins with GitHub, Docker, Kubernetes, Ansible, Terraform  
- Adding Jenkins credentials for authentication  
- Sending notifications via Slack, Email, Webhooks  

🔗 **Resources:**  
- [Jenkins GitHub Integration](https://docs.github.com/en/actions/automating-builds-and-tests/automating-ci-cd-with-github-actions)  
- [Jenkins Kubernetes Plugin](https://plugins.jenkins.io/kubernetes/)  

💻 **Hands-on Exercise:**  
1. Set up a **GitHub Webhook** to trigger Jenkins builds automatically.  
2. Integrate **Jenkins with Docker** and push images to Docker Hub.  

---

## **📌 Part 6: Mock Interview Questions (1 Hour)**  
1. Explain the difference between Continuous Integration, Continuous Delivery, and Continuous Deployment.  
2. How does Jenkins differ from GitHub Actions or GitLab CI/CD?  
3. What is a Jenkinsfile, and why is it used?  
4. How can you set up a Jenkins job to deploy applications automatically?  
5. How do you secure Jenkins and manage credentials?  

---

### **🎯 End-of-Day Checklist:**  
✅ Installed Jenkins and configured plugins  
✅ Created Jenkins jobs and ran basic builds  
✅ Set up a working CI/CD pipeline  
✅ Integrated Jenkins with GitHub & Docker  
✅ Practiced interview questions  

---

