# Getting Started with MkDocs and Material Theme

This tutorial will walk you through setting up a documentation site using [MkDocs](https://www.mkdocs.org/) and the [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/) theme. It is aimed at beginners who want to create a professional-looking static site for documentation using Markdown.

## Prerequisites

- Python 3.7 or higher installed
- Git installed
- Basic familiarity with the command line

## Steps

1. **Create a project directory**

    ```bash
    mkdir my-docs-site
    cd my-docs-site
    ```

2. **Create and activate a virtual environment**

    ```bash
    python3 -m venv .venv
    source .venv/bin/activate
    ```

3. **Install MkDocs and the Material theme**

    ```bash
    pip install mkdocs mkdocs-material
    ```

4. **Scaffold a new MkDocs site**

    ```bash
    mkdocs new .
    ```

5. **Create additional folders for documentation content**

    ```bash
    mkdir -p docs/tutorials docs/howto docs/reference docs/explanations
    ```

6. **Create Markdown files for each documentation section**

    ```bash
    touch docs/tutorials/getting-started.md
    touch docs/howto/write-functional-spec.md
    touch docs/reference/functional-spec-template.md
    touch docs/explanations/diataxis.md
    ```
    
7. **Edit the MkDocs configuration file**

    Open the mkdocs.yml file and make sure it includes the following structure:

    ```yaml
    site_name: "Elisa (E) Morales Cinta — Technical Author Portfolio"
    site_description: "Diátaxis-style documentation samples (tutorial, how-to, reference, explanation)"
    repo_name: "elimrls/technical-author-portfolio"
    nav:
        - Home: index.md
        - Diátaxis:
            - Tutorials: tutorials/getting-started.md
            - How-to: howto/write-functional-spec.md
            - Reference: reference/functional-spec-template.md
            - Explanations: explanations/diataxis.md
    theme:
        name: material
    extra_css:
        -styles/fix-list-code.css
    ```

8. **Preview the site locally**

    Run the following command:

    ```bash
    mkdocs serve
    ```

    Then open your browser and visit:

    ```
    http://127.0.0.1:8000
    ```

## Next Steps

Now that your MkDocs site is running, you can begin writing and organizing your documentation using the Diátaxis framework: tutorials, how-to guides, reference material, and explanations.

---
