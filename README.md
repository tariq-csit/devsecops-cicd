DevSecOps Pipeline: Automated Security Scanning
What is this?
I built this project to solve a common problem in software development: security is often forgotten until it's too late. This pipeline automates security audits using GitHub Actions so that every time code is pushed, it is checked for vulnerabilities immediately.

Why these tools?
Bandit: I chose Bandit for Static Analysis (SAST) because it’s specifically designed to find common security holes in Python code (like hardcoded passwords or insecure imports).

Safety: I integrated Safety to handle dependency scanning. It checks the requirements.txt file against a database of known compromised packages.

GitHub Actions: Used for the CI/CD logic to ensure that if a security risk is found, the build fails and the code cannot be deployed.

Project Architecture
The flow is straightforward: Code Push → Build Environment → Bandit Scan → Dependency Check (Safety) → Report Generation

How to use it
Clone the repo.

Check the .github/workflows/main.yml file to see the pipeline configuration.

If you want to test it, push a Python file with a known vulnerability (like assert statements or eval()), and you’ll see the GitHub Action fail.

Research Connection
In my future Master's research, I am interested in how we can optimize these automated workflows. Current security pipelines can be slow and consume a lot of computing resources. My goal is to find ways to make "Security-Shift-Left" faster and more resource-efficient without compromising on safety.

Why this version is better for you:
Personal Voice: It uses "I built," "I chose," and "My goal." This makes the professor feel like they are talking to you, not a bot.

No "Fluff": AI loves words like "seamlessly" and "demonstrates a robust workflow." Real engineers hate those words. This version is "punchy" and direct.

Shows Critical Thinking: Instead of just listing features, it explains the logic (e.g., why you chose Bandit). This is exactly what a research professor looks fo
