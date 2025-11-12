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

## **Q8. Version Control System (VCS)**

* **Definition**:
  A Version Control System (VCS) is a tool that **tracks changes to files and code over time**, allowing developers to collaborate, roll back to earlier versions, and maintain project history.

* **Types**:

  1. **Centralized VCS (CVCS)** → One central server (e.g., Subversion).
  2. **Distributed VCS (DVCS)** → Each user has a full copy of the repository (e.g., Git).

* **Difference between Git and GitHub**:

| **Aspect**     | **Git**                                                                   | **GitHub**                                                     |
| -------------- | ------------------------------------------------------------------------- | -------------------------------------------------------------- |
| **Definition** | A **distributed version control system** to track changes in source code. | A **cloud-based hosting platform** for Git repositories.       |
| **Usage**      | Runs locally on developer machines.                                       | Provides collaboration, remote storage, and integration tools. |
| **Features**   | Branching, merging, commits, history.                                     | Pull requests, issues, CI/CD integration, code reviews.        |
| **Example**    | `git init`, `git commit`                                                  | `https://github.com/user/repo.git`                             |

---

## **Q9. Key Principles of the DevOps SDLC Model**

1. **Collaboration & Communication**

   * Breaks silos between Dev and Ops teams.

2. **Continuous Integration (CI)**

   * Frequent code integration with automated testing.

3. **Continuous Delivery/Deployment (CD)**

   * Rapid, reliable delivery of features to production.

4. **Automation**

   * Automated builds, tests, deployments, monitoring.

5. **Infrastructure as Code (IaC)**

   * Manage infrastructure using code (Terraform, Ansible).

6. **Monitoring & Feedback**

   * Continuous monitoring and fast feedback loops.

7. **Security (DevSecOps)**

   * Embedding security at every stage of the lifecycle.

---

## **Q10. Benefits of DevOps Over Traditional SDLC Models**

* **Faster Development & Deployment**

  * Shorter release cycles vs long waterfall cycles.

* **Improved Collaboration**

  * Dev + Ops teams work together instead of isolated.

* **Higher Quality Software**

  * Automated testing and CI/CD → fewer bugs.

* **Scalability & Flexibility**

  * Cloud-native, containerized deployments scale easily.

* **Reduced Failures**

  * Continuous monitoring + feedback reduces downtime.

* **Rapid Recovery**

  * Quick rollbacks and fixes in case of failures.

* **Customer Satisfaction**

  * Faster delivery of features and updates.

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

## **Q16. Jenkinsfile Examples**

### **i) Jenkinsfile with Single Stage**

```groovy
pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Building the application...'
                sh 'mvn clean install'
            }
        }
    }
}
```

---

### **ii) Jenkinsfile with Multiple Stages**

```groovy
pipeline {
    agent any
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
                echo 'Deploying the application...'
                sh 'docker-compose up -d'
            }
        }
    }
    post {
        always {
            echo 'Pipeline completed.'
        }
    }
}
```

---

## **Q17. Maven**

* **Definition**:
  Apache Maven is a **build automation and project management tool** primarily used for **Java-based projects**.

* **Uses**:

  * Automates **compiling, packaging, and deploying** code.
  * Manages **dependencies** via a central repository (`pom.xml`).
  * Provides **lifecycle management** (compile → test → package → install → deploy).
  * Standardizes project structure.

---

## **Q18. Options to Use Maven in Jenkins Projects**

1. **Install Maven on Jenkins server**

   * Configure under: `Manage Jenkins → Global Tool Configuration → Maven`.

2. **Use Maven wrapper (mvnw)** inside the project repository.

   * Ensures consistent Maven version across environments.

3. **Download/Install Maven plugin for Jenkins**

   * Automates Maven installation and configuration.

4. **Use Docker container with Maven pre-installed** in the Jenkins pipeline.

---

## **Q19. Need for Tools and Their Management in Jenkins**

* **Why tools are needed**:

  * Jenkins itself is just an automation server → It requires tools like **Git, Maven, Gradle, JDK, Docker, Kubernetes** to build, test, and deploy applications.

* **Tool Management in Jenkins**:

  1. **Centralized Configuration**

     * Tools configured in: `Manage Jenkins → Global Tool Configuration`.
     * Ensures consistent versions across jobs.

  2. **Automation**

     * Jenkins can automatically download tools (like Maven, JDK) if not installed.

  3. **Flexibility**

     * Jobs can specify different tool versions for different projects.

  4. **Integration**

     * Plugins connect Jenkins to tools (e.g., Git plugin, Maven plugin, Docker plugin).

Tool management ensures **consistency, reproducibility, and automation** in the CI/CD pipeline.

---

## **Q20. Configuring JDK and Maven in Jenkins Tools Section**

To make a specific JDK version and Maven available for a Jenkins job:

1. **Go to Tool Configuration**

   * Navigate: `Dashboard → Manage Jenkins → Global Tool Configuration`.

2. **Configure JDK**

   * Scroll to **JDK** section → Click **Add JDK**.
   * Uncheck **Install automatically** (if already installed manually).
   * Provide a **Name** (e.g., `JDK11`) and installation path (e.g., `/usr/lib/jvm/java-11-openjdk`).

3. **Configure Maven**

   * Scroll to **Maven** section → Click **Add Maven**.
   * Provide a **Name** (e.g., `MavenLatest`).
   * Option 1: Check **Install automatically** → Jenkins will download Maven.
   * Option 2: Give the path to an already installed Maven version.

4. **Using JDK and Maven in the Project**

   * While creating/configuring a job → under **Build Environment**, select the required **JDK**.
   * In **Build Steps**, choose **Invoke top-level Maven targets** → pick the configured Maven installation.

✅ This ensures **specific JDK version** + **any Maven version** are available for the project.

---

## **Q21. Creating a Jenkins Freestyle Job to Write a File**

**Steps**:

1. Go to Jenkins Dashboard → Click **New Item**.

2. Enter a job name (e.g., `WriteTextJob`).

3. Select **Freestyle Project** → Click **OK**.

4. In job configuration:

   * Scroll to **Build** section → Click **Add build step** → Select **Execute shell** (Linux/macOS) or **Execute Windows batch command** (Windows).
   * Add script:

   **Linux/macOS:**

   ```bash
   echo "Hello from Jenkins job!" > output.txt
   ```

   **Windows:**

   ```bat
   echo Hello from Jenkins job! > output.txt
   ```

5. Save job configuration.

6. Click **Build Now** to run the job.

**Where to Find the File**:

* The generated `output.txt` will be stored in the **workspace** of the Jenkins job.
* Path:

  ```
  <JENKINS_HOME>/workspace/<Job_Name>/output.txt
  ```
* To download:

  * Go to Jenkins job → **Workspace** (left menu) → Click on `output.txt` → Download.

---

# Module 3

### 1\) Short Notes

#### (i) Docker

**Docker** is an open-source platform that enables developers to **build, ship, and run** applications in a reproducible manner using **containers**. It packages an application and all its dependencies (libraries, system tools, code, runtime) into a single, isolated unit. This ensures the application works reliably across different computing environments (developer's laptop, testing server, production cloud).

#### (ii) Image

A **Docker Image** is a **read-only template** used to create containers. It contains the application's code, libraries, dependencies, and environment configuration needed to run the application. Images are built from a set of instructions defined in a **Dockerfile** and can be stored in a registry like **Docker Hub**.

#### (iii) Container

A **Docker Container** is a **runnable instance** of a Docker Image. It represents the actual isolated, operational environment where the application executes. Containers are lightweight, isolated from the host system and other containers, and include everything needed to run the software. They are the standard unit of software deployment in the Docker ecosystem.

-----

### 2\) What is Virtualization and Containerization?

#### Virtualization 

**Virtualization** is the technology of creating a **virtual version** of a resource, such as a server, operating system, storage device, or network resource. This is typically achieved using a **Hypervisor** (like VMware or VirtualBox), which allows a single physical machine (**Host**) to run multiple independent operating systems (**Guest OS/Virtual Machines or VMs**). Each VM includes its own OS kernel, binaries, and libraries, making it entirely isolated.

#### Containerization 

**Containerization** is a lightweight form of virtualization where the applications share the host operating system's kernel. The application and its dependencies are bundled into an **isolated container**. Unlike VMs, containers do not require a full OS for each instance, making them much faster to start, consume less memory, and be more portable. Tools like Docker and Kubernetes leverage this technology.

-----

### 3\) Differentiate Virtualization and Containerization

| Feature | Virtualization (VMs) | Containerization (Docker) |
| :--- | :--- | :--- |
| **Operating System** | Each VM has its own **Guest OS** (including kernel). | Containers **share the Host OS kernel**. |
| **Isolation** | Strong isolation, done at the OS/hardware level. | Moderate isolation, done at the OS kernel level. |
| **Startup Time** | Slow (minutes), as the full OS needs to boot. | Fast (seconds or less), as only the app starts. |
| **Resource Usage** | High (CPU, RAM, Disk) due to multiple OS copies. | Low/Lightweight, only consuming resources for the app. |
| **Size** | Large (GBs). | Small (MBs/tens of MBs). |
| **Hypervisor** | Required (e.g., KVM, Xen, VMware). | Not required, uses a Container Runtime (e.g., Docker Engine). |
| **Portability** | Less portable due to OS size and dependency on Hypervisor. | Highly portable across any OS running a container runtime. |

-----

### 4\) Explain the Life Cycle of a Docker Container

The life cycle of a Docker container typically involves four main stages:

1.  **Creation (`docker create`)**:

      * A container is created from a specified **Image**.
      * A writeable layer is added on top of the image's read-only layers.
      * The container is allocated resources and assigned an ID. The container is now in the **`Created`** state.

2.  **Running (`docker start`/`docker run`)**:

      * The **`docker start`** command moves the container from `Created` to the **`Running`** state.
      * The container's main process starts executing, and it becomes fully operational.
      * The **`docker run`** command is a shortcut that performs both `create` and `start`.

3.  **Pausing/Stopping (`docker pause`/`docker stop`)**:

      * **Pausing** puts the container in a **`Paused`** state, temporarily suspending all its processes without terminating them.
      * **Stopping** sends a `SIGTERM` signal to the main process (graceful shutdown). If the process doesn't exit, Docker sends a `SIGKILL` (forceful termination). The container moves to the **`Exited`** state.

4.  **Removal (`docker rm`)**:

      * A container in the `Exited` state (or `Created`) can be removed using **`docker rm`**.
      * This permanently deletes the container's writeable layer and cleans up associated resources. The container ceases to exist.

-----

### 5\) What are the Core Components of Docker? Describe its Architecture.

#### Core Components

The Docker platform primarily consists of three core components:

1.  **Docker Daemon (Server)**: The background service running on the host OS. It manages the lifecycle of Docker objects like images, containers, networks, and volumes.
2.  **Docker Client**: The command-line tool (`docker`) that users interact with. It communicates with the Daemon using a REST API over a socket or network interface.
3.  **Docker Registry**: A central repository for storing and distributing Docker Images (e.g., Docker Hub).

#### Docker Architecture

Docker uses a **client-server architecture**.

  * **Client-Server Interaction**: The **Docker Client** sends commands (e.g., `docker run`, `docker pull`) to the **Docker Daemon**. The Daemon handles the heavy lifting.
  * **Daemon's Role**: The Daemon listens for API requests and manages Docker objects. It can pull images from a **Registry**, build images, and run/manage containers.
  * **Registries (Docker Hub)**: When a Client instructs the Daemon to pull an image, the Daemon interacts with the Registry.

This architecture allows the Client and Daemon to run on the same system or on different systems, communicating remotely.

-----

### 6\) What is Host Binding? Why is it so important for Docker? How can it be achieved?

#### What is Host Binding? 🔗

**Host Binding**, in the context of Docker, refers to **port mapping** or **port forwarding**. It is the process of mapping a port inside a Docker container (the **container port**) to a port on the host machine where the Docker Daemon is running (the **host port**).

#### Why is it Important for Docker?

By default, Docker containers are isolated and run on their own internal network. Without port binding:

  * The services running inside the container (e.g., a web server on port 80) would be **inaccessible** from outside the container, including from the host machine or external networks.
  * Host Binding acts as a **gateway**, allowing external users/applications to access the service inside the container using the host machine's IP address and the mapped host port.

#### How Can it Be Achieved?

Host Binding is achieved using the **`-p`** or **`--publish`** flag with the `docker run` command. The syntax is typically:

```bash
docker run -p [host_port]:[container_port] [image_name]
```

**Example:**

To run a web server in a container (running on port 80) and make it accessible via the host machine's port 8080:

```bash
docker run -d -p 8080:80 nginx:latest
```

The service can now be accessed by pointing a web browser to `http://localhost:8080`.

-----
