# docker-nginx-alpine-webpage
# 🚀 Ahmed Kamel - First DevOps Project

> A simple static website served via **Nginx** in a **Docker** container.

![Nginx](https://img.shields.io/badge/Nginx-009639?style=for-the-badge&logo=nginx&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)

![webpage](/docker-1st-project.png)
---

## 👤 About Me

**Ahmed Kamel**  
🔗 [LinkedIn Profile](https://www.linkedin.com/in/eng--ahmed-kamel/)  
💼 DevOps Engineer | Cloud Enthusiast | Automation Lover

---

## 📋 Project Overview

This project demonstrates a basic DevOps workflow:
- ✅ Create a static HTML page
- ✅ Containerize it using **Nginx:alpine**
- ✅ Run the container with Docker
- ✅ Serve content via host port `8080`
- ✅ Use volume mounting for live code updates

---

## 🛠️ Setup & Deployment Commands

Below are the commands used to build and run this project:

```bash
# 1. Create project directory
mkdir 1st-Project
cd 1st-Project/

# 2. Create/edit the HTML file
vim index.html

# 3. Verify file and location
ls
pwd

# 4. Check available Docker images
docker images

# 5. Run Nginx container with volume mapping
docker run -it -d \
  --name html \
  -p 8080:80 \
  -v /home/ozi/Docker-Course/projects/1st-Project:/usr/share/nginx/html \
  nginx:alpine

# 6. Verify container is running
docker ps

# 7. Update content anytime (live reload via volume)
vim index.html
