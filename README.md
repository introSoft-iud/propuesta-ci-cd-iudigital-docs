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

---
Última actualización: 2025-07-25
