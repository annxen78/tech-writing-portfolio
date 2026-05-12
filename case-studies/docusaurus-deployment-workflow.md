# Documentation Handover: iBox Documentation System

## 1. Purpose

This document describes the current iBox documentation workflow, including content storage, site generation, and deployment setup.

---

## 2. Documentation Storage

### Documentation Website


The documentation website is hosted on Netlify.

---

### Public GitHub Repository

Documentation content was managed through GitHub repositories using a docs-as-code workflow.

This repository is connected to the deployment workflow and contains:

- the `docs/` directory with Markdown content
- Docusaurus configuration
- sidebar and navigation structure

---

### Internal Repository

A separate internal repository was used as a private company copy of the documentation.

This repository was not connected to deployment workflows.

---

## 3. Repository Synchronization

Synchronization between the public and internal repositories was handled manually.

### Git Workflow

The local repository was configured with two remotes:

- `origin` — internal repository
- `public` — public GitHub repository used for deployment

After updates, changes were pushed manually:

```bash
git push origin main
git push public main
```


## 4. Deployment Workflow

1. Documentation updates are pushed to the public GitHub repository.
2. Netlify automatically starts a new build process.
3. Docusaurus generates the static documentation website.
4. The updated version is published on Netlify.

### Documentation Website

A documentation website was generated and deployed using Docusaurus and Netlify.

---

## 5. Netlify Configuration

### Build Command

`npm run build`

### Publish Directory

`build`

### Deploy Branch

`main`

### Framework

Docusaurus (static site generator)

## 6. Rebuilding the Website from Scratch

To redeploy the documentation on a new Netlify account:

1. Create a new Netlify project.
2. Select **Import from Git**.
3. Connect the required GitHub repository.
4. Configure the following settings:

- Build command: `npm run build`
- Publish directory: `build`

5. Start deployment.

After configuration, the documentation website can operate independently from the original Netlify account.

---

## 7. Content Management

Documentation content is written in Markdown.

### Main structure files

- `sidebars.js`
- `docusaurus.config.js`

Adding new articles does not require deployment workflow changes.

---

## 8. Notes and Recommendations

At the moment, deployment is connected to a repository hosted under a personal GitHub account because that repository is linked to Netlify.

To reduce operational risks, the following improvements were recommended:

- move deployment to a company-owned Netlify account
- or add a company administrator with deployment access

