# DevOps
1. About Jenkins
Jenkins is an open-source automation server used to automate software building, testing, and deployment. It is widely used in CI/CD pipelines to reduce manual work and deliver software changes faster.
Key points to remember
- Type: Open-source automation server.
- Purpose: Automates build, test, and deployment processes.
- Language: Jenkins pipelines are commonly written using Groovy-based Pipeline syntax.
- Interface: Web-based dashboard.
- Default port: 8080.
- Configuration file: Jenkinsfile (for Pipeline-as-Code).
- Plugins: Extend Jenkins functionality by integrating tools such as Git, Maven, Docker, and SonarQube.
- Supported platforms: Linux, Windows, macOS, and containers.
2. What is CI/CD?
- CI — Continuous Integration: Developers frequently push code changes to a shared repository. Jenkins can automatically retrieve the code and run builds and tests.
- CD — Continuous Delivery: Automatically prepares and validates the application for release.
- CD — Continuous Deployment: Automatically deploys validated changes to production without requiring a separate manual release approval.
3.# Jenkins
## Jenkins Installation
### Step 1: Install Java
#### Verify Java Version
4.## Jenkins Components

- Controller
- Agent
- Pipeline
- Jenkinsfile
- Plugins

5.3. Jenkins Workflow

Developer pushes code to GitHub.

GitHub triggers Jenkins using a webhook.

Jenkins pulls the code.

Jenkins builds and tests the application.

Jenkins deploys the application.


6.How jenkins pulls code from github
  Step-by-step explanation
1. Configure GitHub in Jenkins: Create a Pipeline job and provide the GitHub repository URL.
2. Configure credentials: If the repository is private, configure a suitable credential, such as a personal access token or SSH key, in Jenkins.
3. Trigger the job: Jenkins can start manually, on a schedule, through SCM polling, or through a webhook.
4. Pull the code: The Jenkins Git plugin checks out the configured branch into the workspace.
5. Execute the pipeline: Jenkins runs the commands in the Jenkinsfile.

7.Whats happen internally 

1.First checkout: Git typically clones the repository into the workspace.

2.Subsequent builds: Jenkins can fetch new changes and check out the required commit instead of cloning everything from scratch.

3.Webhook: It notifies Jenkins that a change occurred; it does not transfer the source code itself. Jenkins retrieves the code after the job starts.
