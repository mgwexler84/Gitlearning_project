# Learning Roadmap: From HTML to Full-Stack CI/CD

## Overview
Build a web application incrementally, learning modern development and delivery practices at each step.

---

## Phase 1: Hello World + Git Basics
**Status: IN PROGRESS**
- [x] Initialize git repository
- [x] Create `.gitignore`
- [x] Create `index.html` (simple hello world)
- [x] First commit
- [ ] Practice branching and merging

**Concepts**: git init, staging, commits, branches, merge, git log, .gitignore

---

## Phase 2: GitHub + Remote Collaboration
**Status: IN PROGRESS**
- [x] Create GitHub repository
- [x] Connect local repo to remote
- [x] Push code to GitHub
- [ ] Create a feature branch, make changes, open a PR
- [ ] Review and merge the PR

**Concepts**: remotes, push/pull, pull requests, code review, GitHub UI

---

## Phase 3: Continuous Integration (CI)
**Status: NOT STARTED**
- [ ] Add GitHub Actions workflow
- [ ] Lint/validate HTML
- [ ] Run checks automatically on PRs
- [ ] Fix a failing check and re-push

**Concepts**: CI pipelines, YAML config, automated checks, status checks on PRs

---

## Phase 4: Continuous Deployment (CD) — Static Site
**Status: NOT STARTED**
- [ ] Deploy to GitHub Pages (or Netlify/Vercel)
- [ ] Automate deployment on merge to main
- [ ] See changes go live automatically

**Concepts**: CD pipelines, environments, deploy-on-merge, hosting

---

## Phase 5: Project Structure — Separation of Concerns
**Status: NOT STARTED**
- [ ] Split into separate HTML, CSS, and JS files
- [ ] Organize into a `src/` directory
- [ ] Update CI/CD pipeline for new structure

**Concepts**: file organization, separation of concerns, project conventions

---

## Phase 6: Build Tooling
**Status: NOT STARTED**
- [ ] Initialize npm project (`package.json`)
- [ ] Add Vite as a build tool
- [ ] Dev server with hot reload
- [ ] Production build output
- [ ] Update CI/CD to use build step

**Concepts**: npm, package management, dev vs prod builds, bundling

---

## Phase 7: Backend — Client-Server Architecture
**Status: NOT STARTED**
- [ ] Add Node.js/Express backend
- [ ] Create API endpoints
- [ ] Frontend calls backend API
- [ ] Monorepo or separate client/server folders

**Concepts**: REST APIs, client-server model, HTTP methods, JSON, project structure

---

## Phase 8: Database + Secrets
**Status: NOT STARTED**
- [ ] Add a database (SQLite -> PostgreSQL)
- [ ] Database migrations
- [ ] Environment variables and secrets management
- [ ] Update CI/CD with secrets handling

**Concepts**: data persistence, migrations, .env files, GitHub secrets, 12-factor app

---

## Phase 9: Containerization
**Status: NOT STARTED**
- [ ] Write a Dockerfile
- [ ] Docker Compose for local multi-service dev
- [ ] Container-based CI pipeline
- [ ] Container registry

**Concepts**: containers, images, Docker Compose, reproducible environments

---

## Phase 10: Cloud Deployment
**Status: NOT STARTED**
- [ ] Deploy to cloud provider (AWS, GCP, or similar)
- [ ] Multi-service architecture in production
- [ ] Monitoring and logging basics
- [ ] Full CI/CD pipeline: commit -> test -> build -> deploy

**Concepts**: cloud infrastructure, production deployment, observability, full pipeline

---

## Progress Log
<!-- Add entries as we complete milestones -->
| Date | Phase | Milestone | Notes |
|------|-------|-----------|-------|
| 2026-03-05 | 1 | Git init, .gitignore, index.html, first commit | Learned staging area, commit workflow |
| 2026-03-05 | 1 | Added style.css, practiced staging two files | Saw how git tracks new vs modified files differently |
| 2026-03-05 | 2 | Installed gh CLI, created GitHub repo, pushed | Learned remotes, origin, push, linking local to remote |
