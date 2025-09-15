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

## **Q6.A. Command to Check Difference Between Staging Area and Local Copy**

* Command:

```bash
git diff
```

* **Explanation**:

  * Shows changes between the **working directory (local copy)** and the **staging area**.
  * If you want to see changes between **staging area and last commit**, use:

    ```bash
    git diff --cached
    ```

---

## **Q6.B. Command to View the History of Commits**

* Command:

```bash
git log
```

* **Options**:

  * `git log --oneline` → Shows commit history in short form.
  * `git log --graph --oneline --decorate --all` → Shows commit history in a visual graph.

---

## **Q6.C. How to Roll Back to Your Previous Commit**

Several ways depending on use case:

1. **Soft Reset** (keep changes staged):

```bash
git reset --soft HEAD~1
```

2. **Mixed Reset** (keep changes in working directory):

```bash
git reset --mixed HEAD~1
```

3. **Hard Reset** (discard changes completely):

```bash
git reset --hard HEAD~1
```

4. **Checkout Previous Commit (read-only)**:

```bash
git checkout <commit_id>
```

5. **Revert Commit (creates new commit that undoes previous one)**:

```bash
git revert <commit_id>
```

---

## **Q6.D. Difference Between `git revert` and `git reset`**

| **Aspect**   | **git revert**                                        | **git reset**                                       |
| ------------ | ----------------------------------------------------- | --------------------------------------------------- |
| **Action**   | Creates a new commit that undoes the specified commit | Moves HEAD pointer to a previous commit             |
| **History**  | Preserves history (safe for shared repos)             | Rewrites history (can cause issues in shared repos) |
| **Use Case** | Safely undo a commit in public repositories           | Roll back local changes or delete commits           |
| **Command**  | `git revert <commit_id>`                              | `git reset --soft/mixed/hard <commit_id>`           |

---

## **Q7.A. Steps to Connect Local Git Repository with Remote Repository**

1. **Initialize a local repository** (if not already done):

```bash
git init
```

2. **Add files & commit**:

```bash
git add .
git commit -m "Initial commit"
```

3. **Add the remote repository URL**:

```bash
git remote add origin <remote_repo_url>
```

*(Example: `git remote add origin https://github.com/user/project.git`)*

4. **Verify the remote**:

```bash
git remote -v
```

5. **Push local commits to remote repository**:

```bash
git push -u origin main
```

*(Replace `main` with branch name if different)*

---

## **Q7.B. Difference Between `git fetch` and `git pull`**

| **Aspect**   | **git fetch**                             | **git pull**                                     |
| ------------ | ----------------------------------------- | ------------------------------------------------ |
| **Action**   | Downloads commits/branches from remote    | Downloads + merges changes into local branch     |
| **Merging**  | Does **not** merge automatically          | Automatically merges into current branch         |
| **Use Case** | Safe way to see what’s new before merging | Directly update local branch with remote changes |
| **Command**  | `git fetch origin`                        | `git pull origin main`                           |

---

## **Q7.C. Steps to Avoid Merge Conflicts**

1. **Always pull latest changes before starting new work**:

```bash
git pull origin main
```

2. **Work on separate feature branches** instead of directly on `main`.

3. **Commit changes frequently** with clear messages.

4. **Communicate with team** to avoid editing the same files simultaneously.

5. **Use smaller, focused commits** → easier to merge.

6. **Resolve conflicts locally before pushing**:

   * Check conflict with:

     ```bash
     git status
     ```
   * Open file, manually fix `<<<<<<<` and `>>>>>>>` markers.
   * Stage and commit after resolving:

     ```bash
     git add <file>
     git commit -m "Resolved merge conflict"
     ```

---

# Module 2

## **Q1. What is Continuous Integration? How can Jenkins help us to achieve it?**

### **Continuous Integration (CI)**

* **CI** is the practice of **merging all developers’ code changes frequently** (several times a day) into a shared repository.
* Each integration is automatically **built and tested** to detect errors early.
* Benefits:

  * Early bug detection.
  * Faster development.
  * Ensures code always remains in a deployable state.

### **How Jenkins Helps in CI**

* Jenkins is an **open-source automation server**.
* It automates:

  1. **Code fetching** from GitHub/GitLab.
  2. **Building** the project (Maven/Gradle).
  3. **Running automated tests** (JUnit, Selenium).
  4. **Providing reports** (success/failure).

**Example Jenkins CI Job Flow**:

```
Developer → Push code to GitHub → Jenkins detects changes → Build → Test → Report
```

---

## **Q2. What is Continuous Delivery?**

* **Continuous Delivery (CD)** ensures that **code is always in a deployable state**, after passing through automated builds and tests.
* The software is not deployed automatically but is **ready for release anytime**.
* Requires a **manual approval step** before production deployment.
* **Goal:** Minimize risk and make deployments routine and reliable.

---

## **Q3. What is Continuous Deployment and Continuous Delivery? How can Jenkins help us to achieve these?**

### **Continuous Deployment**

* Every code change that passes automated tests is **automatically deployed to production**.
* No manual approval is needed.
* Ensures rapid and frequent releases.

### **Continuous Delivery**

* Code is **kept deployable at all times** but **requires manual approval** to deploy.
* Safer for organizations that want human checks before production.

### **How Jenkins Helps**

* Jenkins can be configured with **pipelines** to:

  * **Build → Test → Package → Deploy** automatically.
  * Use plugins like Docker, Kubernetes, AWS, Ansible to deploy applications.
* With Jenkins:

  * **Continuous Delivery** = automated pipeline until "ready for deployment", then manual approval.
  * **Continuous Deployment** = fully automated pipeline including production release.

---

## **Q4. Difference Between Continuous Deployment and Continuous Delivery**

| **Aspect**       | **Continuous Delivery**                           | **Continuous Deployment**                      |
| ---------------- | ------------------------------------------------- | ---------------------------------------------- |
| Deployment       | Manual approval before production release         | Automatic release to production                |
| Automation Level | Build, test, staging automated; production manual | Build, test, staging, production all automated |
| Risk Level       | Lower (human approval step)                       | Higher (fully automated, immediate changes)    |
| Goal             | Software always deployable                        | Users always get latest changes                |

---

## **Q5. Create a Jenkins Pipeline to Push Local Repository to GitHub**

### **Sample Jenkinsfile**

```groovy
pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/username/repository.git'
            }
        }

        stage('Build') {
            steps {
                sh 'echo "Building project..."'
                // Example: sh 'mvn clean install'
            }
        }

        stage('Test') {
            steps {
                sh 'echo "Running tests..."'
                // Example: sh 'mvn test'
            }
        }

        stage('Push to GitHub') {
            steps {
                withCredentials([usernamePassword(credentialsId: 'github-creds', usernameVariable: 'USER', passwordVariable: 'PASS')]) {
                    sh '''
                        git config user.email "you@example.com"
                        git config user.name "Your Name"
                        git add .
                        git commit -m "Automated commit from Jenkins"
                        git push https://${USER}:${PASS}@github.com/username/repository.git main
                    '''
                }
            }
        }
    }
}
```

### **Explanation**

* **Checkout stage** → Pulls repo from GitHub.
* **Build & Test stages** → Compile & test project.
* **Push stage** → Commits and pushes code back to GitHub.
* **withCredentials** → Uses Jenkins stored credentials (`github-creds`).

---

## **Q6. Workflow to Achieve CI/CD in Jenkins**

### **Steps**

1. **Developer pushes code** → Code is committed to GitHub/GitLab.
2. **Jenkins detects changes** (via webhook or polling).
3. **Build stage** → Jenkins compiles code (e.g., Maven/Gradle).
4. **Test stage** → Unit, integration, and regression tests run.
5. **Package stage** → Build artifacts (e.g., JAR, WAR, Docker image).
6. **Deploy stage** → Code is deployed to staging/production environment.
7. **Monitor stage** → Application monitored with Prometheus/Grafana.

### **Workflow Diagram (Textual)**

```
Developer → GitHub → Jenkins Build → Jenkins Test → Jenkins Deploy → Production → Monitor
```

---

## **Q7. Jenkins Architecture for CI/CD**

### **Components**

1. **Jenkins Master**

   * Central server that manages jobs, schedules builds, and monitors slaves.
   * Provides web UI (dashboard).
   * Stores job configuration and plugin management.

2. **Jenkins Slave (Agent)**

   * Executes jobs assigned by the master.
   * Can run on different OS, environments, or containers.
   * Useful for distributed builds.

### **Architecture Flow**

```
           +------------------+
           |   Jenkins Master |
           +------------------+
             |    Schedules
             v
     +------------------+   +------------------+
     | Jenkins Slave 1  |   | Jenkins Slave 2  |
     | (Linux Build)    |   | (Windows Build)  |
     +------------------+   +------------------+
             |
             v
         Build / Test / Deploy
```

---

## **Q8. Steps to Check Log File After Starting the BUILD for a Jenkins Job**

1. Open Jenkins Dashboard.
2. Click on the **Job Name** you triggered.
3. Select the specific **Build Number** (e.g., `#15`).
4. Click **Console Output**.
5. The **log file** will display build progress, errors, or success messages in real time.

---

## **Q9. Need for Jenkins Master-Slave Architecture**

* **Scalability** → Distributes build jobs across multiple agents.
* **Load balancing** → Prevents single machine overload.
* **Cross-platform builds** → Run builds on different OS (Linux, Windows, macOS).
* **Faster execution** → Parallel builds across multiple slaves.
* **Flexibility** → Slaves can be provisioned dynamically in the cloud (e.g., AWS EC2, Kubernetes).

---

## **Q10. Role of the Slave in Master-Slave Architecture**

* **Execution agent** that runs build/test/deploy tasks assigned by the master.
* **Reports status** (success/failure) back to master.
* Can be configured for **specific environments** (e.g., one slave with Java, another with Python).
* **Parallelism** → Multiple slaves allow concurrent builds.
* Example:

  * Slave 1 → Builds Java application.
  * Slave 2 → Runs Selenium UI tests.
  * Slave 3 → Deploys Docker containers.

---

## **Q11. Essential Components of the Jenkins Master**

* **Job Scheduler** → Schedules and assigns build jobs to slaves/agents.
* **Web UI/Dashboard** → Provides graphical interface to manage jobs, builds, and configurations.
* **Configuration Manager** → Stores job configurations, credentials, and environment details.
* **Plugin Manager** → Handles installation, updates, and removal of plugins.
* **Build Queue** → Maintains pending build requests.
* **Security Manager** → Controls authentication, authorization, and user permissions.
* **Executor (on master node)** → Runs builds directly (though usually jobs run on slaves).

---

## **Q12. Plugins in Jenkins**

* **Definition** → Plugins are extensions that enhance Jenkins functionality.
* **Value Addition**

  * Integrate with tools (Git, Maven, Gradle, Docker, Kubernetes).
  * Enable CI/CD pipeline stages (Build, Test, Deploy).
  * Provide UI enhancements (e.g., Blue Ocean plugin).
  * Add integrations with cloud platforms (AWS, GCP, Azure).
  * Support monitoring, notifications (Slack, Email).

---

## **Q13. Steps for Plugin Management in Jenkins**

**i) Check for plugins already installed**

* Navigate to: `Dashboard → Manage Jenkins → Manage Plugins → Installed` tab.

**ii) Search for a particular plugin**

* Go to: `Dashboard → Manage Jenkins → Manage Plugins → Available` tab.
* Enter plugin name in the **Search box**.

**iii) Install the plugin**

* Select the plugin → Click **Install without restart** (or **Download now and install after restart**).

**iv) Restart Jenkins after installation**

* Option 1: Run in browser → `http://<your-server>:8080/restart`
* Option 2: From CLI →

  ```bash
  sudo systemctl restart jenkins
  ```
* Option 3: After installation, check “Restart Jenkins when installation is complete”.

---

## **Q14. Jenkins File**

* A **Jenkinsfile** is a text file that defines a Jenkins pipeline using **Groovy DSL**.
* Stored in the project repository (`Jenkinsfile`).
* Benefits:

  * Code-as-configuration → Pipeline versioned with source code.
  * Standardization → Same build/deploy process for all team members.
  * Automation → Full CI/CD pipeline execution.

---

## **Q15. Typical Structure of a Jenkins File**

Example **Declarative Pipeline**:

```groovy
pipeline {
    agent any     // Run on any available agent
    stages {
        stage('Build') {
            steps {
                echo 'Building the application...'
                sh 'mvn clean install'
            }
        }
        stage('Test') {
            steps {
                echo 'Running tests...'
                sh 'mvn test'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying application...'
                sh 'docker-compose up -d'
            }
        }
    }
    post {
        success {
            echo 'Pipeline executed successfully.'
        }
        failure {
            echo 'Pipeline failed.'
        }
    }
}
```

### **Structure Breakdown**

1. **pipeline** → Root block.
2. **agent** → Defines execution node.
3. **stages** → Multiple stages like Build, Test, Deploy.
4. **steps** → Commands executed inside each stage.
5. **post** → Actions after pipeline (success/failure).

---
