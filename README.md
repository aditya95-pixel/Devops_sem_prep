# Module 1

## **Q1.A. Explain the Waterfall Model and its Challenges**

### **Waterfall Model**

* The **Waterfall Model** is a traditional **sequential software development model**.
* Each phase must be completed before moving to the next.
* Phases: **Requirement → Design → Implementation → Testing → Deployment → Maintenance**.

### **Diagram**

```
Requirements → Design → Implementation → Testing → Deployment → Maintenance
```

### **Challenges**

* **Rigid**: No feedback loops, hard to go back once a phase is complete.
* **Late Testing**: Errors are found very late in the cycle.
* **Slow Delivery**: Working software is available only at the end.
* **Customer Dissatisfaction**: Requirements may change, but model does not handle changes well.
* **High Risk**: Failure in one stage impacts the entire project.

---

## **Q1.B. Main Stages of the DevOps Life Cycle**

The **DevOps Life Cycle** integrates development and operations through continuous processes:

1. **Plan** → Define requirements, backlog, user stories.
2. **Code** → Develop software using VCS (e.g., Git).
3. **Build** → Compile code, create artifacts, run unit tests.
4. **Test** → Automated testing (unit, integration, regression).
5. **Release** → Prepare for production, approval gates.
6. **Deploy** → Deploy to production or staging automatically.
7. **Operate** → Manage infrastructure, ensure reliability.
8. **Monitor** → Track performance, logs, metrics, incidents.
9. **Feedback** → Continuous improvement based on monitoring results.

### **Diagram (Infinity Loop)**

```
Plan → Code → Build → Test → Release → Deploy → Operate → Monitor → (back to Plan)
```

---

## **Q1.C. One Tool for Each Stage of the DevOps Life Cycle**

| **Stage** | **Tool Example**        |
| --------- | ----------------------- |
| Plan      | Jira, Trello            |
| Code      | Git, GitHub             |
| Build     | Maven, Gradle           |
| Test      | Selenium, JUnit         |
| Release   | Jenkins, GitHub Actions |
| Deploy    | Docker, Kubernetes      |
| Operate   | Ansible, Puppet         |
| Monitor   | Prometheus, Grafana     |

---

Here’s the exam-ready Markdown answer for **Q2** 👇

---

## **Q2.A. What is Git?**

* **Git** is a **distributed version control system (VCS)** used to track changes in source code.
* Created by **Linus Torvalds** in 2005 for Linux kernel development.
* Key features:

  * **Distributed**: Every developer has a full copy of the repository.
  * **Efficient branching & merging**.
  * **Keeps history of changes** (commits).
  * **Collaboration** using platforms like GitHub, GitLab, Bitbucket.

---

## **Q2.B. Git Life Cycle**

### **States in Git**

1. **Working Directory** → Your local files (can be modified).
2. **Staging Area (Index)** → Selected changes that will go into the next commit.
3. **Local Repository** → Committed snapshots stored in `.git`.
4. **Remote Repository** → Central/shared repo (e.g., GitHub).

### **Diagram**

```
Working Directory  →  Staging Area  →  Local Repository  →  Remote Repository
   (git add)            (git commit)         (git push)
   (git checkout)       (git reset)          (git fetch/pull)
```

### **Explanation**

* **git add** → Moves changes from Working Directory → Staging Area.
* **git commit** → Saves staged changes into Local Repository.
* **git push** → Uploads local commits to Remote Repository.
* **git pull/fetch** → Downloads changes from Remote Repository.
* **git checkout** → Switch branches or restore files.

---

## **Q2.C. Branching and Merging in Git**

### **Branching**

* A **branch** is a lightweight movable pointer to a commit.
* Default branch is usually **main** or **master**.
* Allows parallel development (e.g., feature branch, bug-fix branch).

Example:

```bash
git branch feature-login
git checkout feature-login
```

### **Merging**

* **Merge** combines changes from one branch into another (e.g., merging feature branch into main).
* Command:

```bash
git checkout main
git merge feature-login
```

### **Merge Conflicts**

* Occur when **two branches modify the same part of a file differently**.
* Git cannot automatically decide which change to keep.
* Developer must **manually resolve** conflicts.

**Example of conflict:**

```diff
<<<<<<< HEAD
print("Hello from main branch")
=======
print("Hello from feature branch")
>>>>>>> feature-login
```

---

