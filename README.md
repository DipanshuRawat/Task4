
# 🚀 DevOps Git Workflow Documentation

## 🧠 What is Git and GitHub?

**Git** is a distributed version control system used to track changes in source code during software development. It helps multiple developers collaborate efficiently by managing code changes, branches, and merges.

**GitHub** is a cloud-based hosting service for Git repositories. It provides tools for collaboration, code review, issue tracking, and CI/CD integration, making project development and management easier for teams of all sizes.

---

This markdown documents the Git-based version control workflow followed for our DevOps project.

---

## ✅ Step 1: Git Repository Setup

Initialized Git and pushed to GitHub.

```bash
git init
git remote add origin https://github.com/your-username/devops-project.git
git add .
git commit -m "Initial commit"
git push -u origin main
```

📸 **Screenshot: GitHub Repo Initialized**  
![Screenshot (480)](https://github.com/user-attachments/assets/d2690745-337a-46ba-bf1d-31742f053ca2)


---

## ✅ Step 2: Created `dev` Branch & Added File

```bash
git checkout -b dev
echo "This is dev branch" > dev.txt
git add dev.txt
git commit -m "dev branch"
git push -u origin dev
```

📸 **Screenshot: Dev Branch Created**  
![Screenshot 2025-04-11 113140](https://github.com/user-attachments/assets/2c5aa3e9-0fcf-4160-9baf-1a44f2f85780)


---

## ✅ Step 3: Created `feature` Branch & Added Files

```bash
git checkout -b feature/login
echo "Login feature file" > login.txt
git add login.txt
git commit -m "This is from feature branch"
git push -u origin feature/login
```

📸 **Screenshot: Feature Branch Created**  
![Screenshot 2025-04-11 113206](https://github.com/user-attachments/assets/77329b15-4b0b-47a0-ab0d-e583a3612e29)


---

## ✅ Step 4: Pull Request - Feature ➝ Dev

- Open a pull request from `feature/login` to `dev`.
- Review and approve the pull request.
- Merge changes.

📸 **Screenshot: PR from Feature to Dev**  
![Screenshot (489)](https://github.com/user-attachments/assets/f953f2ca-2f03-4041-bcd2-53f5ee3039ae)

![Screenshot (490)](https://github.com/user-attachments/assets/73ab4ba6-cf5f-48cb-be73-3f0fe9d92cdf)

![Screenshot (491)](https://github.com/user-attachments/assets/cb999474-8d84-409a-ad85-1506bbcd94e2)

![Screenshot (492)](https://github.com/user-attachments/assets/dbb44d1a-63d4-4ad4-a344-d042da98df68)

![Screenshot (493)](https://github.com/user-attachments/assets/f2545320-d5b6-4fc0-aedb-ee16ffdb86da)

---

## ✅ Step 5: Pull Request - Dev ➝ Main

- Open a pull request from `dev` to `main`.
- Review and approve the pull request.
- Merge changes.

📸 **Screenshot: PR from Dev to Main**  
![Screenshot (494)](https://github.com/user-attachments/assets/e3d74d2e-49eb-46d3-923f-23772894b49c)

![Screenshot (495)](https://github.com/user-attachments/assets/6220ff32-2beb-48d4-98a2-b75353e3190e)

![Screenshot (496)](https://github.com/user-attachments/assets/b95ffed9-9222-4f5f-92f5-bc266274a27b)

![Screenshot (497)](https://github.com/user-attachments/assets/f5e0871c-5dd5-480d-9e37-9d36e32ff4f0)

---

## ✅ Step 6: Added `.gitignore`

Added a `.gitignore` file to ignore unnecessary files.

```bash
touch .gitignore
```

**Sample Contents**:
```
node_modules/
.env
*.log
*.tfstate
__pycache__/
```

📸 **Screenshot: .gitignore File**  
![Screenshot 2025-04-11 115141](https://github.com/user-attachments/assets/8ea27b02-c6bf-4fc2-8550-12a4baa2dfaa)

---

## ✅ Step 7: Added Git Tags

Tagged the first release as `v1.0`.

```bash
git tag -a v1.0 -m "Initial release"
git push origin v1.0
```

📸 **Screenshot: Tag Created**  
![Screenshot 2025-04-11 115141](https://github.com/user-attachments/assets/d4b96776-f89e-4894-9bc1-445d51cafb85)

![Screenshot (498)](https://github.com/user-attachments/assets/c2d0a5de-9d33-4610-8127-0d23d7a40254)

---

## 📁 Final Branch Strategy

- `main` — Production branch  
- `dev` — Development/integration branch  
- `feature/*` — Feature-specific branches  

---

> ✨ Follow Git best practices: 
- small atomic commits,
- meaningful messages,
- feature branching
- pull requests for collaboration and code review.
