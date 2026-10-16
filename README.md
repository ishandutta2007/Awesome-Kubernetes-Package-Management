# Awesome-Kubernetes-Package-Management

## Top Kubernetes Package Management Ecosystem



**Curated List of SaaS Products & Open-Source GitHub Projects**  

*Focused on Application Packaging, Templating & GitOps Delivery*  

**Last updated: October 2026**



This repository tracks notable **SaaS platforms** and **open-source projects** for **Kubernetes Package Management**. These tools template, package, distribute, and deploy applications to Kubernetes — from chart-based package managers like Helm to CUE-powered alternatives, YAML-overlay tools, and GitOps-native deployment frameworks.



**Examples** include Helm, Kustomize, Argo CD, Flux, Carvel, Timoni, Glasskube, Devtron, and Skaffold (the category leaders).



**Open-source emphasis**: This section is heavily expanded with every major active project for self-hosting, GitOps-native delivery, and transparent package management — ideal for platform engineers, DevOps teams, and organizations building vendor-neutral Kubernetes delivery pipelines.



Contributions welcome! Open an PR to add/update entries. Keep descriptions factual and link to official sites.



## Table of Contents

- [SaaS/Hosted Platforms](#saas-hosted-platforms)

- [Open-Source GitHub Projects](#open-source-github-projects)

- [How to Contribute](#how-to-contribute)

- [Disclaimer](#disclaimer)



## SaaS/Hosted Platforms



- **[Argo CD](https://argo-cd.readthedocs.io/)**  

  Declarative GitOps continuous delivery tool for Kubernetes; the de facto standard for GitOps-based application deployment with a strong UI and multi-cluster support .



- **[Flux CD](https://fluxcd.io/)**  

  GitOps toolkit from the CNCF with a modular controller-based architecture; the original GitOps operator and direct competitor to Argo CD .



- **[Devtron](https://devtron.ai/)**  

  Open-source Kubernetes delivery platform with a GUI for Helm-based application management, CI/CD, and security scanning.



- **[Octopus Deploy](https://octopus.com/)**  

  Deployment automation platform with Kubernetes support for managing releases across environments.



- **[Cloudsmith](https://cloudsmith.io/)**  

  Universal package management with OCI/Docker registry support for hosting Helm charts and Kubernetes artifacts.



- **[JFrog Artifactory](https://jfrog.com/artifactory/)**  

  Universal artifact repository manager supporting Helm chart repositories and OCI registries for Kubernetes package distribution.



- **[Harbor](https://goharbor.io/)**  

  Open-source cloud native registry with Helm chart repository support and OCI artifact management.



- **[Glasskube Cloud](https://glasskube.dev/cloud)**  

  Managed offering for Glasskube with private packages, security alerts, and advanced GitOps integrations (in development) .



## Open-Source GitHub Projects



- **[Helm](https://github.com/helm/helm)**  

  **The de facto Kubernetes package manager** — 28,000+ stars, CNCF Graduated. Uses Go templates and `values.yaml` to generate Kubernetes manifests from reusable "charts." Supports chart repositories (HTTP/OCI), release tracking, rollbacks, hooks, and dependency management. The standard for installing third-party software like Prometheus, NGINX Ingress, and cert-manager .



- **[Kustomize](https://github.com/kubernetes-sigs/kustomize)**  

  **Template-free configuration customization** — built into `kubectl` since v1.14. Uses `kustomization.yaml` overlays to patch base YAML without modifying originals. No templating language to learn; ideal for environment promotion (base → dev → staging → production). Native GitOps integration .



- **[Carvel (ytt, kapp, kbld, imgpkg)](https://github.com/carvel-dev/carvel)**  

  **The "Swiss Army Knife" of Kubernetes configuration** — a set of single-purpose, composable tools. `ytt` provides YAML-structure-aware templating with Starlark (Python-like) instead of text substitution; `kapp` deploys resources as a single application with change-set previews; `kbld` resolves images to immutable digests; `imgpkg` bundles config and images as OCI artifacts for air-gapped environments. Apache 2.0 licensed .



- **[Timoni](https://github.com/stefanprodan/timoni)**  

  **Helm alternative powered by CUE** — 1,300+ stars, Apache 2.0. Uses CUE's type safety, code generation, and validation instead of Go templates mixed with YAML. Modules distributed as OCI artifacts (signable with Cosign), server-side apply, staged resource application, CRD templating and upgrades (which Helm ignores), and health checks on custom resources. Still in active development with potentially breaking API changes .



- **[Glasskube](https://github.com/glasskube/glasskube)**  

  **Homebrew/npm-style package manager for Kubernetes** — YC-backed, aims to make deploying, updating, and configuring packages 20x faster than Helm. Type-safe package configurations via UI or interactive CLI, safe package updates pre-tested by Glasskube, GitOps integration (all packages are custom resources), and dependency management. Apache 2.0 licensed .



- **[Skaffold](https://github.com/GoogleContainerTools/skaffold)**  

  **Continuous development for Kubernetes** — handles building, pushing, and deploying applications with a single `skaffold dev` command. Supports Helm, Kustomize, and raw YAML as deployment renderers. Excellent for local development inner-loop .



- **[Tilt](https://github.com/tilt-dev/tilt)**  

  **Local development environment for Kubernetes** — smart rebuilds, live updates, and a UI showing service health. Accelerates inner-loop development for microservices.



- **[Garden](https://github.com/garden-io/garden)**  

  **Automation for Kubernetes development and testing** — uses a declarative config to define stacks, with smart caching and dependency-aware builds.



- **[Argo CD](https://github.com/argoproj/argo-cd)**  

  **GitOps continuous delivery** — CNCF Graduated, the dominant GitOps tool. Declarative, Git-based deployment with auto-sync, drift detection, multi-cluster management, and a rich UI .



- **[Flux CD](https://github.com/fluxcd/flux2)**  

  **GitOps toolkit** — CNCF Graduated, modular controller-based architecture. Supports Helm Controller, Kustomize Controller, and source controllers for Git/OCI/Helm repositories .



- **[kapp-controller (Carvel)](https://github.com/carvel-dev/kapp-controller)**  

  **Continuous delivery and package management for Kubernetes** — captures application deployment workflows in an App CRD, enabling GitOps-style continuous delivery with Carvel tools .



- **[Kubeapps](https://github.com/vmware-tanzu/kubeapps)**  

  **Web-based UI for deploying and managing Helm charts and Carvel packages** in Kubernetes clusters. Browse catalogs, deploy with custom values, and manage releases.



### Additional Strong Open-Source Options



- **[kpt](https://github.com/GoogleContainerTools/kpt)** — Kubernetes package toolkit with KRM Functions for declarative configuration management .

- **[KubeVela](https://github.com/kubevela/kubevela)** — Application delivery platform with OAM-based abstractions for defining and deploying apps.

- **[Crossplane](https://github.com/crossplane/crossplane)** — Declarative infrastructure provisioning as Kubernetes resources; complements package management for infrastructure automation.

- **[Kubernetes Operators](https://operatorhub.io/)** — OperatorHub catalogs hundreds of Kubernetes Operators that extend the API for application-specific lifecycle management.

- **[Sherpack](https://github.com/alegeay/sherpack)** — Helm-like package manager with Jinja2 templating, written in Rust. Features `lookup()` for reading cluster state, idempotent secret generation, and superior CRD management (templated CRDs, managed/shared/external policies) .

- **[app2kube](https://github.com/n0madic/app2kube)** — Generates production-ready manifests from a minimal app definition with safe-by-default hardening (security contexts, probes, resource baselines) .

- **[octoploy](https://pypi.org/project/octoploy/)** — Simple templating engine with folder-based app definitions, variable inheritance, and configmap file watching .

- **[frank-cli](https://github.com/schnauzersoft/frank-cli)** — Stateless, packageless, template-driven Kubernetes management with Jinja and HCL templating .



**Frameworks for building custom systems**: The **standard trio** is **Helm** for third-party packages (charts), **Kustomize** for your own applications (overlays), and **Argo CD** or **Flux** for GitOps delivery . For teams seeking alternatives to Go templates, **Carvel** provides YAML-structure-aware templating with Starlark, while **Timoni** leverages CUE for type-safe configuration. For a Homebrew-like experience, **Glasskube** offers type-safe package management with a UI.



**Key architectural insight**: Helm remains the only widely-adopted tool for consuming packaged third-party software . Kustomize is built into `kubectl` and maps naturally to GitOps directory structures. Many teams use both: Helm to render third-party charts, Kustomize to patch them, then Argo CD or Flux to sync to the cluster. The lack of interoperability between configuration managers remains the main obstacle to adoption of alternatives .



## How to Contribute



1. Fork the repo.

2. Add/edit entries in `README.md` (follow existing format).

3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.

4. Submit PR with a short explanation.



Star the repo if you find it useful!



## Disclaimer



- This is a **community-curated** list — not exhaustive and not an endorsement.

- **License awareness**: Helm, Kustomize, Carvel, and Timoni are Apache 2.0. Glasskube is Apache 2.0. Verify terms before commercial deployment.

- Self-hosted solutions require Kubernetes operational expertise, proper RBAC configuration, and regular security updates.

- Helm's Go template + YAML combination is powerful but can become complex; Kustomize's overlay approach is simpler but lacks dependency management and rollback features .



---



**Made for platform engineers, DevOps teams, Kubernetes operators, and cloud-native enthusiasts.**  

Let's make Kubernetes package management more open, composable, and vendor-neutral.
