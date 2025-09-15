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
