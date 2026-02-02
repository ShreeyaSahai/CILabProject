# CI Lab Project – Jenkins

## Overview
This project demonstrates Continuous Integration using Jenkins. It includes a Freestyle job and a Multibranch Pipeline connected to a GitHub repository, showing automated builds, tests, artifacts, and branch-based pipelines.

---

## Tools & Technologies
- Jenkins
- GitHub
- Python
- Git
- Windows OS

---

## Installation Guide
1. Install Java (JDK 11+)
2. Install Jenkins and start the service
3. Install required Jenkins plugins (Git, Pipeline, Multibranch Pipeline)
4. Create a GitHub Personal Access Token
5. Add GitHub credentials in Jenkins

---

## Jenkins Job Configuration

### Job 1: Freestyle Project
- Connected to GitHub repository
- Build trigger using Poll SCM
- Build steps:
  - Run Python script
  - Run Python unit tests
- Post-build actions:
  - Archive artifacts
  - Display test results in console
  - Email notification (configured)

### Job 2: Multibranch Pipeline
- Automatically discovers branches (`main`, `feature/*`, `release/*`)
- Uses a Jenkinsfile for pipeline logic
- Different behavior per branch:
  - `main`: full build
  - `feature`: test stage
  - `release`: build and deploy stage

---

## Jenkinsfile
The Jenkinsfile defines branch-based pipeline behavior using conditional stages and is shared across all branches.

---

## Troubleshooting
- **GitHub authentication failed**: Use a Personal Access Token instead of a password
- **Webhook not working**: Jenkins is running locally; Poll SCM is used instead
- **Python not recognized**: Use full path to `python.exe` in Jenkins build steps
- **Branches not visible**: Ensure Jenkinsfile exists in all branches

---

## Results
- Successful automated builds
- Python script execution
- Test execution with console output
- Artifact archiving
- Branch-specific pipeline execution

---

## Conclusion
This project demonstrates core Jenkins CI concepts including job configuration, GitHub integration, automated testing, artifact management, and multibranch pipelines.


