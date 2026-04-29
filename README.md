# Introduction to Docker - Training Materials Repository


This repository contains hands-on examples, exercises, and sample projects for learning Docker from beginner to advanced level.  

## 📚 Repository Structure

```
introduction-to-docker/
├── .github/
│   └── workflows/
│       └── docker-publish.yml         # GitHub Actions CI/CD workflow
├── examples/                           # Hands-on examples and projects
│   └── docker-cicd-github-actions/    # GitHub Actions CI/CD pipeline example
├── hands-on-exercises/                 # Practical exercises for each topic
│   ├── Networks-Exercises.md          # Docker networking exercises
│   ├── Volumes-Exercises.md           # Data persistence exercises
│   ├── Compose-Exercises.md           # Docker Compose exercises
│   ├── Troubleshooting-Exercises.md   # Debugging and troubleshooting exercises
│   └── group-exercise/                # Collaborative microservices project
│       ├── GROUP-EXERCISE-INSTRUCTIONS.md
│       ├── docker-compose.yml
│       └── ...
├── Dockerfiles/                        # Dockerfile examples and best practices
│   ├── Dockerfile.bad-layers          # ❌ Poor layer caching example
│   ├── Dockerfile.good-layers         # ✅ Optimized layer caching
│   ├── Dockerfile.nodejs-multistage   # Multi-stage build example
│   ├── Dockerfile.build-args          # Build arguments example
│   ├── Dockerfile.cmd                 # CMD instruction example
│   ├── Dockerfile.entrypoint          # ENTRYPOINT instruction example
│   ├── Dockerfile.entrypoint-cmd      # ENTRYPOINT + CMD best practice
│   └── README.md                      # Detailed Dockerfile examples guide
└── README.md                           # This file
```

---

## 🎯 What's Inside

### 1. Hands-On Exercises

**Location:** [`hands-on-exercises/`](hands-on-exercises/)

Four comprehensive exercise sets covering core Docker concepts:

#### **Docker Networks** ([Networks-Exercises.md](hands-on-exercises/Networks-Exercises.md))
- 5 progressive exercises + challenge
- Bridge, host, and custom networks
- Multi-container communication
- Network isolation and DNS
- Real-world microservices networking

#### **Docker Volumes** ([Volumes-Exercises.md](hands-on-exercises/Volumes-Exercises.md))
- 7 progressive exercises + challenge
- Named volumes vs bind mounts
- Database data persistence
- Volume backup and restore
- Development workflows with hot reload
- Read-only mounts and permissions

#### **Docker Compose** ([Compose-Exercises.md](hands-on-exercises/Compose-Exercises.md))
- 6 progressive exercises + challenge
- Multi-container applications
- Service dependencies and networking
- Environment configurations
- Health checks and restart policies
- WordPress, full-stack Node.js apps

#### **Troubleshooting** ([Troubleshooting-Exercises.md](hands-on-exercises/Troubleshooting-Exercises.md))
- 7 practical debugging scenarios
- Container startup failures
- Out of memory issues
- Network connectivity problems
- Volume and permission issues
- Log analysis techniques
- Multi-container debugging

#### **Group Exercise** ([group-exercise/](hands-on-exercises/group-exercise/))
- Collaborative 4-team microservices project
- Each team builds and pushes a service to Docker Hub
- Final integration with docker-compose
- Simulates real-world team workflows

### 2. Dockerfile Examples

### 2. Dockerfile Examples

**Location:** [`Dockerfiles/`](Dockerfiles/)

**What it demonstrates:**
- ✅ Optimized layer caching (good vs bad examples)
- ✅ Multi-stage builds for smaller images
- ✅ Build arguments and environment variables
- ✅ CMD vs ENTRYPOINT best practices
- ✅ Real-world Node.js application patterns

**Key files:**
- `Dockerfile.bad-layers` - Shows what NOT to do (slow rebuilds)
- `Dockerfile.good-layers` - Optimized caching (3-second rebuilds!)
- `Dockerfile.nodejs-multistage` - Production-ready multi-stage build
- `Dockerfile.build-args` - Configuration with build arguments
- `Dockerfile.entrypoint-cmd` - Best practice for CMD + ENTRYPOINT

**Documentation:**
- [Dockerfiles/README.md](Dockerfiles/README.md) - Complete guide with examples

### 3. CI/CD with GitHub Actions

**Location:** [`examples/docker-cicd-github-actions/`](examples/docker-cicd-github-actions/)

**What it demonstrates:**
- Complete GitHub Actions CI/CD pipeline
- Automated Docker image builds
- Testing in containers
- Push to GitHub Container Registry (ghcr.io)
- Automatic version tagging
- Security scanning with Trivy

**Technologies:**
- Docker & Multi-stage builds
- GitHub Actions
- Node.js & Express.js
- GitHub Container Registry

**Quick Start:**
```bash
cd examples/docker-cicd-github-actions
docker build -t demo:local .
docker run -p 3000:3000 demo:local
```

**Documentation:**
- [README](examples/docker-cicd-github-actions/README.md) - Complete setup guide
- [QUICK-START](examples/docker-cicd-github-actions/QUICK-START.md) - 5-minute walkthrough
- [TRAINING-GUIDE](examples/docker-cicd-github-actions/TRAINING-GUIDE.md) - Full workshop guide

---

## 🚀 Getting Started

### Prerequisites

- Docker Desktop installed
- Git installed
- GitHub account (for CI/CD examples)
- Basic command line knowledge

### Clone This Repository

```bash
git clone https://github.com/Emre-Yavas/introduction-to-docker.git
cd introduction-to-docker
```

### Explore Examples

Each example has its own README with:
- ✅ Learning objectives
- ✅ Step-by-step instructions
- ✅ Hands-on exercises
- ✅ Troubleshooting guide
- ✅ Best practices

---

## 📖 Learning Path

**Recommended order:**

1. **Dockerfile Basics** ⭐ **Start here!**
   - Go to `Dockerfiles/` folder
   - Study layer caching examples (bad vs good)
   - Learn multi-stage builds
   - Practice with build arguments

2. **Docker Networks**
   - Complete exercises in `hands-on-exercises/Networks-Exercises.md`
   - Learn bridge, host, and custom networks
   - Practice container-to-container communication

3. **Docker Volumes**
   - Complete exercises in `hands-on-exercises/Volumes-Exercises.md`
   - Master data persistence
   - Practice backup and restore

4. **Docker Compose**
   - Complete exercises in `hands-on-exercises/Compose-Exercises.md`
   - Build multi-container applications
   - Work on the collaborative group exercise

5. **Troubleshooting**
   - Complete exercises in `hands-on-exercises/Troubleshooting-Exercises.md`
   - Learn debugging techniques
   - Practice fixing common issues

6. **CI/CD with GitHub Actions** ⭐ **Advanced!**
   - Go to `examples/docker-cicd-github-actions/`
   - Set up automated workflows
   - Deploy to container registries

---

## 🎓 Who Is This For?

- **Beginners:** Step-by-step guides with detailed explanations
- **Intermediate:** Best practices and real-world patterns
- **DevOps Engineers:** Production-ready CI/CD pipelines
- **Developers:** Integrate Docker into development workflow

---

## 🔧 Technologies Covered

- **Docker:** Containerization, images, multi-stage builds, layer optimization
- **Networking:** Bridge networks, custom networks, DNS, service discovery
- **Storage:** Named volumes, bind mounts, data persistence, backups
- **Compose:** Multi-container apps, service dependencies, orchestration
- **CI/CD:** GitHub Actions, automated workflows, container registries
- **Troubleshooting:** Debugging, log analysis, resource monitoring
- **Testing:** Running tests in containers, health checks
- **Security:** Vulnerability scanning, best practices
- **DevOps:** Automation, deployment strategies, team workflows

---

## 📝 Contributing

This is a training materials repository. If you find issues or have suggestions:

1. Open an issue
2. Submit a pull request
3. Share feedback

---

## 📚 Additional Resources

**Official Documentation:**
- [Docker Documentation](https://docs.docker.com/)
- [GitHub Actions Documentation](https://docs.github.com/en/actions)
- [Docker Best Practices](https://docs.docker.com/develop/dev-best-practices/)

**Online Learning:**
- [Play with Docker](https://labs.play-with-docker.com/)
- [Docker Hub](https://hub.docker.com/)

---

## 📬 Contact

**Repository Owner:** Emre Yavaş
**GitHub:** [@Emre-Yavas](https://github.com/Emre-Yavas)

---

## 📄 License

This repository is for educational purposes. See individual examples for specific licenses.

---

## 🎯 Quick Navigation

### Hands-On Exercises
- [Docker Networks Exercises →](hands-on-exercises/Networks-Exercises.md)
- [Docker Volumes Exercises →](hands-on-exercises/Volumes-Exercises.md)
- [Docker Compose Exercises →](hands-on-exercises/Compose-Exercises.md)
- [Troubleshooting Exercises →](hands-on-exercises/Troubleshooting-Exercises.md)
- [Group Exercise (4 Teams) →](hands-on-exercises/group-exercise/)

### Examples & Guides
- [Dockerfile Examples →](Dockerfiles/)
- [Docker CI/CD Example →](examples/docker-cicd-github-actions/)
- [Quick Start Guide →](examples/docker-cicd-github-actions/QUICK-START.md)
- [Training Guide →](examples/docker-cicd-github-actions/TRAINING-GUIDE.md)

### GitHub Actions
- [CI/CD Workflow →](.github/workflows/docker-publish.yml)

**Start learning Docker today!** 🚀
