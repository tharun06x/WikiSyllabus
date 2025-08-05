# Agent Goal
Create a fully structured **University of Oxford Computer Science (BA/MCompSci)** syllabus inside the WikiSyllabus repository using the **University/Branch/Year/Semester** folder layout and a consistent YAML frontmatter + body template.

---

## Context & Ground Rules
- **Learn the schema from the repo.** Follow the folder pattern:  
  `University/Branch/Year/Semester/`  
  For Oxford CS 2025:  
  `Oxford/CS/2025/S1/`, ..., `Oxford/CS/2025/S8/`.
- **File naming inside each semester**: sequential files `01.md`, `02.md`, ... in the recommended order.
- **Fetch and include all official Oxford Computer Science papers (core + options)** taught in each year, mapping them accurately into S1–S8.
- **Paraphrase official descriptions**; include source links in a **References** section. Avoid copying long passages.
- **Licensing & attribution**: Cite the exact Oxford University page(s) for each subject at the bottom under **References**.

---

## Inputs (parameters)
- `university`: `oxford`
- `branch`: `cs`
- `catalog_year`: `2025`
- `track`: `ba/mcompsci`
- `language`: `english`

---

## Deliverables
1. **Degree overview**  
   - Path: `Oxford/CS/2025/overview.md`  
   - Contents:  
     - Track summary (BA/MCompSci split, optional 4th year)  
     - Degree requirement highlights (core courses, options, projects)  
     - Year-by-year structure (Parts A–C mapped to S1..S8)  
     - Links to authoritative Oxford sources.
2. **Per-semester subject files**  
   - Paths: `Oxford/CS/2025/S1/01.md`, ..., `Oxford/CS/2025/S8/...`  
   - One Markdown per **paper taught by Oxford** in that semester.  
   - Include **all** core and optional papers listed for the degree; if optional, mark as `elective` in the **Overview** and mention typical choices.
3. **Validation**  
   - Run `tools/validate_wikisyllabus.py` to ensure layout, required YAML keys, and **References** section in every file.
4. **Commit & PR**  
   - Branch name: `feat/oxford-cs-2025`  
   - Include a checklist and links to Oxford sources used.

---

## Authoritative Oxford sources
- Oxford Computer Science Course Information Sheet 2025  
  <https://www.ox.ac.uk/sites/files/oxford/field/field_document/Computer%20Science%20CIS%202025.pdf>  
- Department of Computer Science – BA/MCompSci structure:  
  - [Part A](https://www.cs.ox.ac.uk/teaching/bacompsci/PartA/)  
  - [Part B](https://www.cs.ox.ac.uk/teaching/bacompsci/PartB/)  
  - [Part C](https://www.cs.ox.ac.uk/teaching/bacompsci/PartC/)  
- Alphabetical list of course descriptions:  
  <https://www.cs.ox.ac.uk/teaching/courses/2024-2025/>  
- Example module: [Databases](https://www.cs.ox.ac.uk/teaching/courses/2024-2025/databases/)

---

## YAML Frontmatter
```yaml
---
university: oxford
branch: cs
version: 2025
semester: <1-8>
course_code: <official-or-short-identifier>
course_title: <full-course-title>
units: n/a
level: <ug-or-m>
prerequisites: [<titles>]
language: english
contributor: akshay-k-a-dev
---
````

---

## File Body Template

1. **Overview** – 3–6 lines paraphrasing Oxford’s catalog description.
2. **Learning Objectives** – concise bullet points.
3. **Syllabus Outline** – weekly/clustered topics; propose if not given.
4. **Assessment & Workload** – exam/project type; note `not-specified-in-source` if absent.
5. **Recommended Texts & Resources** – official Oxford module page(s); supplementary reading if listed.
6. **References** – exact Oxford URL(s) used.

---

## High-Level Plan

1. **Clone & learn**: Understand folder + frontmatter rules from repo.
2. **Fetch Oxford CS data**: Extract **all** core and optional papers for 2025 from official sources.
3. **Map to 8 semesters**:

   * part-a → s1 & s2
   * part-b → s3 & s4
   * part-c → s5 & s6
   * mcompsci-year-4 → s7 & s8.
4. **Generate Markdown**: Follow YAML + body template; include **References**.
5. **Create overview\.md**: Summarize ba/mcompsci structure, requirements, and links.
6. **Validate**: Run validator.
7. **Commit & PR**: Create feature branch, commit, PR.

---

## Acceptance Criteria

* All files in `Oxford/CS/2025/` under `S1..S8`.
* Every subject file has exact YAML keys and **References**.
* `overview.md` explains ba/mcompsci structure, mapping, and links.
* **All papers taught by Oxford** for the degree are included in the relevant semester folders.
* Validator passes with zero errors.

---

## Edge Cases & Notes

* For optional/elective papers, include them in the semester folder and mark `elective` in the **Overview**.
* Oxford does not number courses like MIT; use official title or a short code.
* Units are not used; mark `n/a` but note workload if available.
* Map parts evenly into semesters for repo consistency.

```
