# DevOps Tasks - 2026

Welcome to Team TechnoJam Auditions 2026!!!!!!

We have prepared 3 DevOps tasks according to their respective difficulty levels.

Note: Complete and submit the assigned task according to the instructions provided by the TechnoJam team.

> **Resources:** For reference materials, tools, and helpful links for DevOps, check out `Resources.md`.

---

## Easy - Git and GitHub

### Task: Git Workflow and GitHub

- Create a GitHub repository.
- Create a simple static HTML/CSS website.
- Push the project to GitHub using Git.
- Create a `feature/dev` branch.
- Make some changes to your website on the `feature/dev` branch.
- Push the branch to GitHub.
- Create a Pull Request from `feature/dev` to `main`.
- Merge the Pull Request into `main`.
- Practice the following Git commands:
  - `git merge`
  - `git pull`
  - `git rebase`
  - `git stash`

- Make meaningful commit messages.
- Add screenshots of the important Git and GitHub operations.
- Create a `README.md` explaining the Git commands and workflow you used.

### Bonus

Deploy your static website using GitHub Pages.

### Resources

- [Learn Git and GitHub](https://youtu.be/apGV9Kg7ics?si=rr97MYragdtPtpYb)

---

## Medium - Linux, Nginx and Automation

### Task: Set Up and Manage a Local Linux Web Server

Set up a Linux environment using VirtualBox, VMware, or WSL and use it to host and manage a simple website locally.

### Requirements

- Set up an Ubuntu/Linux environment.
- Create a user and a group.
- Assign appropriate permissions.
- Set up SSH key-based authentication.
- Install and configure Nginx.
- Create a simple HTML/CSS website and host it using Nginx.
- Learn how to start, stop, restart, and check the status of Nginx.
- Explore Nginx logs and identify a basic error.
- Create a Bash script that displays:
  - CPU usage
  - Memory usage
  - Disk usage
  - Nginx status

- Create a backup script that backs up your website files.
- Use `cron` to automatically run the backup script at a scheduled time.
- Document all commands and configurations with screenshots.
- Push your scripts, website, and documentation to GitHub.

### Bonus

Configure Nginx to host two different websites locally.

For example:

```text
site1.local
site2.local
```

### Resources

- [DevOps Bootcamp - EC2, S3, CDNs, Nginx and VMs](https://youtu.be/sSRaakd95Nk?si=Su4QRL70aItzylhV)

---

## Hard - Dockerize and Deploy a Node.js Application

### Task: Dockerize and Deploy a Node.js Website

Create a simple Node.js/Express application, containerize it using Docker, and deploy it using Vercel.

### Requirements

#### Node.js Application

- Create a simple Node.js/Express server.
- Add at least 2 routes.

For example:

```text
GET /
GET /about
```

#### Docker

- Create a `Dockerfile`.
- Create a `.dockerignore` file.
- Build a Docker image.
- Run the application inside a Docker container.
- Map the container port to your local machine.
- Stop and remove the container.
- Rebuild and run the container.
- Check the application logs using Docker commands.

#### Environment Variables

- Use at least one environment variable in your application.
- For example:

```text
PORT=3000
```

- Do not commit your `.env` file or any private credentials.

#### Deployment

- Deploy your Node.js application using Vercel.
- Make sure the deployed application is accessible through a public URL.
- Add the deployed URL to your `README.md`.
- Add the **Docker container/image link** to your `README.md`(Docker Hub or registry URL).
- Add screenshots of:
  - Docker setup
  - Running Docker container
  - Application
  - Vercel deployment
  - Docker Hub (or registry) repository showing the pushed image

### Bonus

Make a change to your application, push it to GitHub, and verify that the deployed application gets updated.

### Resources

- [Learn Docker](https://youtu.be/31k6AtW-b3Y?si=2vmv0YpsT85VOzzP)

---

## Submission Requirements

- Source code
- Scripts
- Docker files
- Docker container/image link (Docker Hub)
- Screenshots
- Documentation
- GitHub repository

Make sure your work is properly documented and that you understand the commands and concepts used in your task.

Good Luck!

**Team TechnoJam**
