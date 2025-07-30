# 📚 Contribution Guide

Thank you for your interest in contributing to this WikiSyllabus Repository! 🙌  
Together, we can make a fully open, searchable, and markdown-based syllabus index for students, teachers, and developers.

---

## 📌 What You Can Contribute

- ✅ **New Syllabus Files**  
  - Add missing course markdowns (`.md`) for different branches, semesters, or years.
- 🛠️ **Fix Errors**  
  - Typos, outdated content, or formatting issues.
- 📘 **Add References**  
  - Useful books, links, or official sources for specific courses.
- 💡 **Improve Structure**  
  - Suggestions for folder naming, file structure, or tagging.

---

## 🗂 Folder & File Naming Convention

- Follow this structure:

```

/university/branch/year/semester/XX.md

```

✅ Example:
```

/ktu/computer-science/2019-23/s8/01.md

````

- ✅ Filenames should always be the **numbers** (e.g., `01.md` , `02.md` , ...).

- All **folder and file names** must be in **lowercase**

- If more than one word, use **hyphens** (not underscores or spaces)

### 🔹 Filenames

- **Use `01.md`, `02.md`, ...** to index courses within a semester
- Do **not** use course code in filename
- Course details like code/title should be inside the **YAML frontmatter**

---

## 📝 Markdown File Format

Each `.md` file must start with YAML frontmatter:

```yaml
---
country: "india"
university: "ktu"
branch: "computer-science"
version: "2019-23"
semester: 8
course_code: "CST402"
course_title: "Distributed Computing"
language: "english"
contributor: "@your-github-username"
---

Follow this by the syllabus content (objectives, content, references, etc.)

```

## 📝 How to Contribute

### 1. **Fork the Repository**
Create your own copy of the repository to work on.

### 2. **Create a New Branch**
```bash
git checkout -b feat/add-CST402
```

### 3. **Add Your Markdown File**

Use the correct folder structure and file naming convention.

### 4. **Commit Your Changes**

```bash
git add .
git commit -m "feat: add CST402 - Distributed Computing"
```

### 5. **Push and Make a Pull Request**

```bash
git push origin feat/add-cst402
```

Then go to GitHub and open a **Pull Request (PR)** to the **dev** branch.

---

## 🔍 Before You Submit

✅ Check if the course already exists.

✅ Double-check formatting and spelling.

✅ Add your GitHub username as `contributor`.

✅ Check spelling, formatting, and completeness
---

## 🤝 Code of Conduct

Be respectful and collaborative. This is a shared space for learning and helping others.

---

## 🙋 Need Help?

Open an [issue](https://github.com/your-repo/issues) or tag `@arjun-ms` in your PR.

---

Together, let’s build the best open academic resource!

