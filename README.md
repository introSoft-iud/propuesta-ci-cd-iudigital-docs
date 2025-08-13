# Propuesta de CI/CD Pipeline para la IUDigital de Antioquia

Este repositorio contiene la documentación del proyecto de investigación: **"Propuesta de CI/CD Pipeline para la producción, mantenimiento y despliegue de los cursos en la IUDigital de Antioquia"**.

La documentación está construida con MkDocs y el tema Material for MkDocs.

## Cómo Usar

1.  Clonar el repositorio.
2.  Asegurarse de tener Python y pip instalados.
3.  Instalar MkDocs y el tema Material:
    ```bash
    pip install mkdocs mkdocs-material mkdocs-mermaid2 pymdown-extensions
    ```
4.  Navegar a la raíz del proyecto y servir la documentación localmente:
    ```bash
    mkdocs serve
    ```
5.  Acceder a la documentación en tu navegador (usualmente http://127.0.0.1:8000/).

## Estructura del Proyecto

* `mkdocs.yml`: Archivo de configuración principal de MkDocs.
* `docs/`: Carpeta que contiene todos los archivos Markdown de la documentación.
    * `index.md`: Página de inicio.
    * `fases/`: Subcarpeta para las diferentes fases del proyecto.
    * `assets/`: Para imágenes, favicon, etc.
    * `css/`: Para estilos CSS personalizados.
    * `javascripts/`: Para scripts JS personalizados.


# GitHub Pages Deployment Guide

This document outlines the automated process for deploying our MkDocs site to GitHub Pages using a GitHub Actions workflow.

---

### 1. The GitHub Actions Workflow

The deployment is managed by a workflow file located at `.github/workflows/deploy.yml`. This file defines a set of steps that automatically run whenever changes are pushed to the `deploy` branch.

The key steps in this workflow are:
* **Checkout code**: Fetches the repository's code.
* **Setup Python**: Configures the Python environment required to run MkDocs.
* **Install dependencies**: Installs MkDocs and the `mkdocs-material` theme.
* **Deploy to GitHub Pages**: Uses the `mkdocs gh-deploy` command to build the site and push the output to the `gh-pages` branch. This is the branch GitHub Pages uses to serve the site.

---

### 2. Configuring GitHub Pages

For this workflow to work, you must enable GitHub Pages in the repository settings.

1.  Go to the **Settings** tab of the repository.
2.  In the left sidebar, click on **Pages**.
3.  Under the "Build and deployment" section, select **Deploy from a branch**.
4.  In the "Branch" dropdown, select `gh-pages` and choose the `/ (root)` folder.
5.  Click **Save**.

The first time you run the workflow, the `gh-pages` branch will be created automatically.

---

### 3. Triggering a Deployment

To deploy your site, all you need to do is push your changes to the **`deploy`** branch.

```bash
# Example: Pushing changes from your local 'main' branch to 'deploy'
git checkout main
# Make your changes and commit them
git checkout deploy
git merge main
git push origin deploy
---
Última actualización: 2025-07-25
