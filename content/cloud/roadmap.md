+++
title = "Cloud Roadmap"
collection = "cloud"
author = "Gemini"
date = 2024-02-18
weight = 112
chapter = false
disableToc = false
pre = "<b>📜</b>"
tags = ["devops", "cloud"]
description = "What are cloud platforms?"
+++


# From Code to Production

Building and deploying applications on the cloud requires moving beyond local environments to master distributed systems, infrastructure automation, and operational safety. This roadmap outlines the core competencies, practical exercises, and architectural decisions required to engineer production-ready cloud systems.

---

## Phase 1: Core Fundamentals & Linux

Before touching cloud platforms, you must master the operating system environment that powers 90%+ of cloud infrastructure.

### Concepts & Definitions
* **Process Management & Daemons:** Understanding how processes run, terminate, and restart (systemd).
* **Linux Networking:** IP addressing, TCP/UDP sockets, DNS resolution, and firewall rules (`iptables` / `ufw`).
* **Permissions & Security:** POSIX file permissions, SSH key-based authentication, and principle of least privilege.
* **Environment Configuration:** Managing runtime variables (`.env`, POSIX environment variables).

### Practice Exercises
1. Provision a minimal Linux virtual machine locally (using Multipass, QEMU, or Docker).
2. Write a systemd service file to keep a custom Node.js, Python, or Go application running continuously on system boot.
3. Configure an SSH jump host and disable password-based root login.

---

## Phase 2: Containerization & Local Simulation

Containers decouple applications from underlying host operating systems, ensuring identical behavior from development to production.

### Concepts & Definitions
* **Namespaces & Cgroups:** Linux kernel features that isolate processes, memory, and CPU.
* **Container Images vs. Containers:** Immutable layered file systems versus running runtime instances.
* **OCI Standards:** Open Container Initiative specifications ensuring interoperability.
* **Multi-stage Builds:** Pattern for separating build-time dependencies from lean runtime artifacts.

### Practice Exercises
1. Write a secure, non-root `Dockerfile` for a web application utilizing multi-stage builds.
2. Build and run the image locally, mapping ports and mounting persistent volumes.
3. Use `docker compose` to orchestrate a multi-container local stack (e.g., Application + PostgreSQL + Redis).

---

## Phase 3: Cloud Architecture & Service Models

Understanding how cloud providers abstract hardware into programmable APIs.

### Concepts & Definitions
* **IaaS vs. PaaS vs. Serverless:** Trade-offs between operational control and management overhead.
* **Virtual Private Cloud (VPC):** Logically isolated networks containing public/private subnets, internet gateways, and route tables.
* **Object Storage vs. Block Storage:** Flat-namespace, globally accessible blobs versus attached block devices requiring a filesystem.
* **Identity and Access Management (IAM):** Role-based access control (RBAC), policies, and service principals.

### Practice Exercises
1. Design a multi-tier network architecture on paper: Public Load Balancer $\rightarrow$ Public Subnet (API Gateway) $\rightarrow$ Private Subnet (Compute) $\rightarrow$ Isolated Subnet (Database).
2. Create an AWS IAM Policy restricting an application to read-only access on a specific S3 bucket prefix.

---

## Phase 4: Infrastructure as Code (IaC)

Manual clickOps configuration in web consoles does not scale. Modern cloud infrastructure is defined entirely as version-controlled code.

### Concepts & Definitions
* **Declarative vs. Imperative:** Describing the *desired* end state versus writing procedural scripts.
* **State Management:** Tracking deployed resources via remote state files, locking, and drift detection.
* **Immutability:** Replacing modified servers rather than in-place patching.

### Practice Exercises
1. Write an OpenTofu or Terraform configuration to provision a VPC, a public subnet, and an EC2 instance / Droplet.
2. Store the state file in a remote backend (e.g., AWS S3 with DynamoDB locking).
3. Parameterize the configuration using variables and output the public IP address.

---

## Phase 5: CI/CD Pipeline Engineering

Automating the path from a git commit to a production deployment.

### Concepts & Definitions
* **Continuous Integration:** Automated linting, unit testing, and artifact building on every merge request.
* **Continuous Deployment:** Automated promotion of verified artifacts to staging and production environments.
* **Blue-Green & Canary Deployments:** Zero-downtime release patterns that route traffic incrementally to new versions.

### Practice Exercises
1. Build a GitHub Actions workflow that triggers on main branch pushes.
2. Configure the pipeline to run tests, build a container image, push it to a registry (e.g., GHCR, Docker Hub, or Cloud Registry), and trigger an infrastructure update.

---

## Phase 6: Observability & Production Operations

Code in production will fail. Visibility into system health is mandatory.

### Concepts & Definitions
* **The Three Pillars of Observability:** Metrics (aggregates), Logs (events), and Traces (request lifecycles).
* **Health Checks & Liveness Probes:** Endpoints used by load balancers to determine pod/instance availability.
* **Rate Limiting & Circuit Breakers:** Defensive patterns to protect downstream services from cascading failures.

### Practice Exercises
1. Implement structured JSON logging within your application.
2. Configure a health check endpoint (`/healthz`) that validates database connectivity.
3. Set up uptime monitoring and alerts for error rate spikes.

---

## Configuring a Project for Cloud Deployment

To transition an application from local development to cloud execution, configure the following components:

1. **Environment Agnostic Configuration:** Read all ports, database connection strings, and secrets from environment variables using standard libraries (e.g., `os.Getenv`, `process.env`). Never hardcode configuration.
2. **Containerization:** Ensure a robust `Dockerfile` exists at the root of the repository with a specified non-root user and explicit entrypoint.
3. **Health Check Probes:** Expose unauthenticated endpoints (`/healthz`, `/readyz`) that verify internal dependencies (database, cache) before returning `200 OK`.
4. **Stateless Architecture:** Ensure the application instances store no session state or uploaded files locally. Persist sessions in Redis/Memcached and uploads directly to Object Storage (S3-compatible APIs).
5. **Database Migration Strategy:** Decouple database schema migrations from application startup routines, executing them as isolated pre-deployment jobs.

---

## Critical Architectural Choices

| Decision Vector | Options | Trade-offs & Selection Criteria |
| :--- | :--- | :--- |
| **Compute Primitive** | Bare VMs / VPS vs. Containers (ECS/K8s) vs. Serverless (Lambda/Cloud Run) | **VMs:** Full control, high maintenance. **Containers:** Portable, excellent balance of control and abstraction. **Serverless:** Zero idle cost, scale-to-zero, potential cold start latency. |
| **Database Strategy** | Managed Relational (RDS/Cloud SQL) vs. Self-Hosted vs. NoSQL | **Managed:** Backups, patching, and scaling handled; higher cost. **Self-Hosted:** Lower cost, high operational risk. **NoSQL:** Optimized for unstructured, high-velocity data. |
| **Deployment Target** | Hyperscaler (AWS/GCP/Azure) vs. Developer Cloud (DigitalOcean/Hetzner/Vercel) | **Hyperscaler:** Massive ecosystem, steep learning curve, enterprise compliance. **Developer Cloud:** Predictable pricing, fast setup, simpler networking. |
| **IaC Tooling** | OpenTofu / Terraform vs. Pulumi vs. Cloud-Native (AWS CDK) | **TF/OpenTofu:** Industry standard, declarative HCL. **Pulumi:** Real programming languages (TypeScript, Python, Go). **CDK:** Tightly coupled to single cloud provider. |