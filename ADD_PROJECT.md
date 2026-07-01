# 🚀 How to Add a New NextWork Project

This guide provides a standardized, step-by-step workflow for adding new project documentations to this repository. Following these steps ensures that the repository remains clean, scalable, and beautifully showcased!

---

## 📋 Step-by-Step Checklist

### 1. Duplicate the Project Template
Create a new folder inside `projects/` using the next sequential number and a descriptive slug. For example, if the last project was `01`, name the new folder `02-project-name`.

You can do this manually or via terminal:
```bash
# Example (Linux/macOS/Git Bash):
cp -r projects/_template projects/02-my-new-project

# Example (Windows PowerShell):
Copy-Item -Path "projects\_template" -Destination "projects\02-my-new-project" -Recurse
```

---

### 2. Add Project Documentation & Assets
Navigate inside your new project folder (`projects/XX-project-name/`) and populate the following required and optional contents:

1. **📄 Markdown Lesson (`README.md`)**
   - Open `README.md` inside your project folder.
   - Fill in your project title, architecture overview, learning objectives, and detailed step-by-step notes.
   - Keeping this file named `README.md` ensures that GitHub automatically renders the lesson when anyone opens the folder!

2. **📑 PDF Lesson Document (`lesson.pdf`)**
   - Export or copy your documented lesson PDF directly into the project folder.
   - Recommended filename: `lesson.pdf` (or `project-name-lesson.pdf`).

3. **🖼️ Images (`images/`)**
   - Place any diagrams, screenshots, or architectural charts used in your lesson into the `images/` directory.
   - Reference them inside your project `README.md` using relative paths: `![Architecture Diagram](./images/architecture.png)`.

4. **💻 Sample Code (`code/` - Optional)**
   - If your project includes configuration files, scripts, or application source code (e.g., Python, Terraform, CloudFormation, HTML/JS), place them inside the `code/` subfolder.

5. **🌐 Live Project Link (`project-link.txt`)**
   - Open `project-link.txt` and paste the direct URL to your live project deployment, cloud app, or demo video.

---

### 3. Update the Root Hub (`README.md`)
Once your project folder is ready, go back to the root directory and open the main `README.md`.

Add a new row to the **Project Showcase Gallery Table** so visitors can discover your project:

```markdown
| **#02** | [**Project Title Here**](./projects/02-project-name/) | ![AWS Cloud](https://img.shields.io/badge/AWS-232F3E?style=flat&logo=amazon-web-services&logoColor=white) | [📄 PDF](./projects/02-project-name/lesson.pdf) <br> [📑 Lesson](./projects/02-project-name/README.md) <br> [💻 Code](./projects/02-project-name/code/) | [🔗 Live Demo](https://example.com) |
```

---

### 4. Commit and Push!
Verify your changes locally and push to GitHub:
```bash
git add .
git commit -m "docs: add NextWork project #02 - [Project Name]"
git push origin main
```

🎉 **Done! Your new project is now live on the showcase hub!**
