---
description: Create a new trip plan project with standard structure
---

To create a new project with the standard structure, follow these steps:

1.  **Ask the user for the project name** (e.g., `taiwan-trip-plan`).
2.  **Create the project directory** in the root of the workspace.
3.  **Create the standard subdirectories**:
    *   `src`
    *   `doc`
    *   `assets`
4.  **Create a basic `README.md`** file in the project directory with the project name as the title.
5.  **Copy the template `index.html`** from an existing project (like `tokyo-trip-plan` or `koren-trip-plan`) or create a new basic one if none exists.
6.  **Notify the user** that the project has been set up.

Example commands using `run_command` (replacing `[project-name]` with the actual name):

```bash
mkdir -p [project-name]/src [project-name]/doc [project-name]/assets
touch [project-name]/README.md
echo "# [Project Name]" > [project-name]/README.md
# Optional: Copy index.html if you want to start with a template
# cp tokyo-trip-plan/index.html [project-name]/index.html
```
