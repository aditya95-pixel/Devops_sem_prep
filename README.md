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


## **Q3.A. Why is the Agile Model Preferred over the Waterfall Model?**

### **Agile Model**

* Iterative and incremental approach.
* Continuous feedback and collaboration with stakeholders.
* Working software delivered in **short cycles (sprints)**.

### **Reasons Agile is Preferred over Waterfall**

1. **Flexibility** → Agile adapts to changing requirements; Waterfall is rigid.
2. **Early Delivery** → Agile delivers working software frequently; Waterfall delivers only at the end.
3. **Customer Satisfaction** → Agile involves customers throughout; Waterfall only at requirements & delivery stages.
4. **Risk Reduction** → Problems are identified early in Agile; in Waterfall, risks appear late.
5. **Collaboration** → Agile emphasizes teamwork & communication; Waterfall has siloed phases.

**Summary Table**

| Aspect               | Waterfall Model      | Agile Model             |
| -------------------- | -------------------- | ----------------------- |
| Process              | Sequential           | Iterative & Incremental |
| Flexibility          | Rigid                | Highly adaptable        |
| Delivery             | At the end           | Continuous (sprints)    |
| Testing              | After implementation | Ongoing in each sprint  |
| Customer Involvement | Low                  | High                    |

---

## **Q3.B. Difference between Lean & Agile Models**

### **Lean Model**

* Origin: Lean manufacturing (Toyota Production System).
* Focus: **Eliminate waste, maximize value, optimize processes**.
* Principles: Reduce bottlenecks, ensure continuous flow, focus on efficiency.

### **Agile Model**

* Origin: Agile Manifesto (2001).
* Focus: **Iterative development, customer collaboration, responding to change**.
* Principles: Working software, collaboration, adaptability.

### **Key Differences**

| **Aspect**   | **Lean**                                   | **Agile**                              |
| ------------ | ------------------------------------------ | -------------------------------------- |
| Origin       | Lean Manufacturing (Toyota)                | Software Development (Agile Manifesto) |
| Focus        | Efficiency & Waste Reduction               | Flexibility & Customer Collaboration   |
| Primary Goal | Deliver value faster with fewer resources  | Deliver working software in iterations |
| Approach     | Optimize workflow & remove non-value tasks | Iterative development with feedback    |
| Tools        | Kanban, Value Stream Mapping               | Scrum, XP, Kanban                      |

---

## **Q4.A. What is DevOps?**

* **DevOps** = **Development + Operations**.
* It is a **culture, set of practices, and tools** that integrates software development (Dev) and IT operations (Ops).
* Goal: **Shorter development cycles, faster delivery, high-quality software, continuous improvement**.
* Key principles:

  * **Collaboration** between Dev & Ops teams.
  * **Automation** of builds, testing, deployment, and monitoring.
  * **Continuous Integration & Continuous Delivery (CI/CD)**.
  * **Feedback loops** for quick improvements.

---

## **Q4.B. Sample DevOps Architecture**

### **Architecture Components**

1. **Source Code Management (SCM)** → Version control with Git.
2. **Build & Integration** → Automated builds using Jenkins, Maven, Gradle.
3. **Testing** → Automated tests (JUnit, Selenium).
4. **Deployment** → Containers (Docker), Orchestration (Kubernetes).
5. **Configuration Management** → Tools like Ansible, Puppet.
6. **Monitoring & Logging** → Prometheus, Grafana, ELK stack.
7. **Collaboration** → Tools like Jira, Slack.

### **Sample Flow (Pipeline)**

```
Plan → Code → Build → Test → Release → Deploy → Operate → Monitor → (Feedback → Plan)
```

---

### **Diagram (Textual Representation)**

```
           +-------------------+
           |    Plan (Jira)    |
           +---------+---------+
                     |
                     v
           +-------------------+
           |   Code (GitHub)   |
           +---------+---------+
                     |
                     v
           +-------------------+
           | Build (Jenkins)   |
           +---------+---------+
                     |
                     v
           +-------------------+
           | Test (Selenium)   |
           +---------+---------+
                     |
                     v
           +-------------------+
           | Release (Jenkins) |
           +---------+---------+
                     |
                     v
           +-------------------+
           | Deploy (Docker)   |
           +---------+---------+
                     |
                     v
           +-------------------+
           | Operate (Ansible) |
           +---------+---------+
                     |
                     v
           +-------------------+
           | Monitor (Grafana) |
           +-------------------+
```

---

### **DevOps Lifecycle Parts**

1. **Plan** → Requirements, backlog (tools: Jira, Trello).
2. **Code** → Development & version control (Git, GitHub).
3. **Build** → Compile & package (Maven, Jenkins).
4. **Test** → Automated testing (Selenium, JUnit).
5. **Release** → Ready for deployment (Jenkins pipelines).
6. **Deploy** → Containers & orchestration (Docker, Kubernetes).
7. **Operate** → Manage infra, ensure uptime (Ansible, Puppet).
8. **Monitor** → Logs & metrics (Prometheus, ELK, Grafana).

---

## **Q5.A. Git Workflow and Commands**

### **Git Workflow Phases**

Git follows a **four-phase workflow** for tracking files:

1. **Working Directory**

   * Files are modified locally.
   * Command:

     ```bash
     git status     # check current changes
     ```

2. **Staging Area (Index)**

   * Selected files are staged (prepared) for commit.
   * Commands:

     ```bash
     git add <file>      # stage a specific file
     git add .           # stage all changes
     ```

3. **Local Repository**

   * Staged changes are committed to the local `.git` repository.
   * Commands:

     ```bash
     git commit -m "Commit message"
     ```

4. **Remote Repository**

   * Local commits are pushed to a shared repository (e.g., GitHub).
   * Commands:

     ```bash
     git push origin <branch>
     git pull origin <branch>   # fetch + merge remote changes
     ```

---

### **Diagram of Git Workflow**

```
Working Directory  --(git add)-->  Staging Area  --(git commit)-->  Local Repo  --(git push)-->  Remote Repo
```

---

## **Q5.B. Different Statuses of a Git File**

A file in Git can be in **four main states**:

1. **Untracked**

   * File is new and not yet tracked by Git.
   * Command:

     ```bash
     git status   # shows "untracked file"
     ```

2. **Modified**

   * File is tracked, but changes have been made and not staged yet.
   * Command:

     ```bash
     git diff <file>
     ```

3. **Staged**

   * File changes are added to the **staging area** (ready to commit).
   * Command:

     ```bash
     git add <file>
     ```

4. **Committed**

   * File is saved permanently in the **local repository**.
   * Command:

     ```bash
     git commit -m "message"
     ```

---

### **Summary Table**

| **Status** | **Meaning**                             | **Command Example**       |
| ---------- | --------------------------------------- | ------------------------- |
| Untracked  | File not tracked by Git                 | `git status`              |
| Modified   | Changes made but not staged             | `git diff`                |
| Staged     | Changes added to index, ready to commit | `git add <file>`          |
| Committed  | Changes saved in local repo permanently | `git commit -m "message"` |

---
