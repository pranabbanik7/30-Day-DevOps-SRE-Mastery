### **🗓 Day 5: GitHub Actions & GitLab CI/CD - CI/CD Pipelines**  

#### **🔹 Goals for the Day:**  
✅ Learn how GitHub Actions and GitLab CI/CD work for DevOps automation  
✅ Set up CI/CD pipelines using both tools  
✅ Automate builds, tests, and deployments  
✅ Understand YAML-based workflow configuration  

---

## **📌 Part 1: Introduction to GitHub Actions & GitLab CI/CD (1 Hour)**  
🔹 **Topics to Cover:**  
- What are GitHub Actions & GitLab CI/CD?  
- Why use these CI/CD tools instead of Jenkins?  
- Key differences between GitHub Actions and GitLab CI/CD  
- Common use cases in DevOps (CI/CD pipelines, Infrastructure Automation, Testing, Security Scans)  
- How GitHub Actions integrates with cloud providers, Kubernetes, Docker, and Terraform  

🔗 **Resources:**  
- [GitHub Actions Overview](https://docs.github.com/en/actions)  
- [GitLab CI/CD Documentation](https://docs.gitlab.com/ee/ci/)  

💻 **Hands-on Exercise:**  
1. Compare features of GitHub Actions and GitLab CI/CD.  
2. Set up a **sample GitHub repository** for testing workflows.  

---

## **📌 Part 2: GitHub Actions Basics (2 Hours)**  
🔹 **Topics to Cover:**  
- What are GitHub Workflows, Jobs, and Actions?  
- Understanding YAML syntax in GitHub Actions  
- Types of GitHub Actions: Predefined, Custom, and Marketplace Actions  
- Secrets and Environment Variables in GitHub Actions  

🔗 **Resources:**  
- [GitHub Actions Syntax](https://docs.github.com/en/actions/using-workflows/workflow-syntax-for-github-actions)  

💻 **Hands-on Exercise:**  
1. Create a `.github/workflows/main.yml` file in a GitHub repository.  
2. Write a simple workflow that runs on a `push` event:  
   ```yaml
   name: CI Pipeline

   on: [push, pull_request]

   jobs:
     build:
       runs-on: ubuntu-latest
       steps:
         - name: Checkout Code
           uses: actions/checkout@v2
         - name: Run a Shell Script
           run: echo "Hello from GitHub Actions!"
   ```  
3. Push the changes and observe the workflow execution in **GitHub Actions Dashboard**.  

---

## **📌 Part 3: Setting Up a Complete CI/CD Pipeline with GitHub Actions (2 Hours)**  
🔹 **Topics to Cover:**  
- Running tests in GitHub Actions  
- Building and pushing Docker images using GitHub Actions  
- Deploying an application to AWS/GCP/Azure/Kubernetes  

🔗 **Resources:**  
- [GitHub Actions for CI/CD](https://docs.github.com/en/actions/guides)  

💻 **Hands-on Exercise:**  
1. Write a GitHub Actions pipeline to:  
   - Build a Docker image  
   - Push it to **Docker Hub** or **GitHub Container Registry**  
   - Deploy the container to Kubernetes (if available)  
2. Example workflow (`.github/workflows/deploy.yml`):  
   ```yaml
   name: CI/CD Pipeline

   on:
     push:
       branches:
         - main

   jobs:
     build:
       runs-on: ubuntu-latest
       steps:
         - name: Checkout Code
           uses: actions/checkout@v2
         - name: Build Docker Image
           run: docker build -t myapp:latest .
         - name: Push to Docker Hub
           run: |
             echo "${{ secrets.DOCKER_PASSWORD }}" | docker login -u "${{ secrets.DOCKER_USERNAME }}" --password-stdin
             docker push myapp:latest
     deploy:
       needs: build
       runs-on: ubuntu-latest
       steps:
         - name: Deploy to Kubernetes
           run: kubectl apply -f k8s-deployment.yml
   ```  
3. Add **Secrets** in GitHub (`DOCKER_USERNAME`, `DOCKER_PASSWORD`).  
4. Push changes and verify that the pipeline runs successfully.  

---

## **📌 Part 4: GitLab CI/CD Fundamentals (2 Hours)**  
🔹 **Topics to Cover:**  
- What is GitLab CI/CD, and how does it work?  
- Understanding `.gitlab-ci.yml` syntax  
- GitLab CI/CD Stages: Build, Test, Deploy  
- Runners in GitLab CI/CD  

🔗 **Resources:**  
- [GitLab CI/CD Configuration](https://docs.gitlab.com/ee/ci/yaml/)  

💻 **Hands-on Exercise:**  
1. Set up a new **GitLab project**.  
2. Create a `.gitlab-ci.yml` file in the repository.  
3. Add the following simple pipeline:  
   ```yaml
   stages:
     - build
     - test
     - deploy

   build:
     stage: build
     script:
       - echo "Building the project..."
   
   test:
     stage: test
     script:
       - echo "Running tests..."
   
   deploy:
     stage: deploy
     script:
       - echo "Deploying application..."
   ```  
4. Push changes and monitor the pipeline execution in GitLab.  

---

## **📌 Part 5: Setting Up a Complete CI/CD Pipeline with GitLab CI/CD (2 Hours)**  
🔹 **Topics to Cover:**  
- Running tests in GitLab CI/CD  
- Building and pushing Docker images  
- Deploying to Kubernetes using GitLab CI/CD  

🔗 **Resources:**  
- [GitLab CI/CD for Kubernetes](https://docs.gitlab.com/ee/user/clusters/)  

💻 **Hands-on Exercise:**  
1. Update `.gitlab-ci.yml` to build and push a Docker image:  
   ```yaml
   image: docker:latest

   services:
     - docker:dind

   variables:
     DOCKER_IMAGE: "myrepo/myapp:latest"

   stages:
     - build
     - deploy

   build:
     stage: build
     script:
       - docker build -t $DOCKER_IMAGE .
       - echo "$CI_REGISTRY_PASSWORD" | docker login -u "$CI_REGISTRY_USER" --password-stdin
       - docker push $DOCKER_IMAGE

   deploy:
     stage: deploy
     script:
       - kubectl apply -f k8s-deployment.yml
   ```  
2. Set up GitLab **CI/CD Variables** for Docker authentication.  
3. Push changes and ensure the pipeline executes correctly.  

---

## **📌 Part 6: Mock Interview Questions (1 Hour)**  
1. What is the difference between GitHub Actions and GitLab CI/CD?  
2. How do you structure a GitHub Actions workflow file?  
3. Explain the stages in GitLab CI/CD and how they work.  
4. How do you pass secrets into GitHub Actions or GitLab CI/CD?  
5. How can you use GitHub Actions/GitLab CI/CD for Kubernetes deployments?  

---

### **🎯 End-of-Day Checklist:**  
✅ Understood CI/CD concepts using GitHub Actions & GitLab CI/CD  
✅ Created GitHub Actions and GitLab CI/CD workflows  
✅ Built and pushed Docker images using both tools  
✅ Deployed applications automatically using CI/CD pipelines  
✅ Practiced interview questions  

---

Would you like to **extend the GitHub Actions & GitLab CI/CD discussion** to cover security scanning, testing strategies, or advanced deployment strategies (Blue-Green, Canary)? 🚀🔥
