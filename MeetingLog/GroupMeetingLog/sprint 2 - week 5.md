# 📅 Meeting Record: Week 3

**Date:** April 10th, 2025  
**Time:** 1PM – 2PM  
**Location:** Online  

---

## 🎯 1. Meeting Objective  
Discuss how to adapt our current static website structure to Jekyll’s modular framework by splitting shared components, keeping `.html` files, and assigning responsibilities for integration and layout construction.

---

## 📋 2. Core Discussion Points

### A. Understanding Jekyll’s Structure Needs  
- Jekyll encourages a **modular architecture**, separating layouts, includes, and page content.  
- Our current website is composed of multiple full `.html` pages, each duplicating elements like `<head>`, navbars, and footers.  
- Instead of converting to Markdown (`.md`), we will **retain the `.html` format**, and simply add [YAML front matter](https://jekyllrb.com/docs/front-matter/) to make pages compatible with Jekyll.

### B. Current Site Structure Review  
We reviewed our existing files and identified the following:

#### 📄 Main HTML Pages:
- `index.html`: Homepage  
- `web_about_us.html`, `web_contact.html`, `web_products.html`: Informational pages  
- `web_AI_trail.html`, `web_sub_AI_trail.html`: Topic-specific pages  
- `web_latest_news.html`, `latest_news.html`: News sections  
- `members.html`: Team introduction  
- `SampleUI.html`: Demo UI (auxiliary)

#### 🎯 Components & Assets:
- `footer.html`: Already modularized  
- `style.css`, `script.js`: Static styling and interactivity files  
- ❌ Missing: `header.html` and `nav.html` (to be extracted)

### C. Refactoring & Integration Plan  
To follow Jekyll’s structure, we proposed the following actions:

| Jekyll Component       | Source File(s)              | Notes                                          |
|------------------------|-----------------------------|------------------------------------------------|
| `_includes/footer.html`| `footer.html`               | Already extracted, no changes needed           |
| `_includes/header.html`| To be extracted             | From `<head>` sections across pages            |
| `_includes/nav.html`   | To be extracted             | Shared navbar across pages                     |
| `_layouts/default.html`| New                         | Will include header, footer, nav, and `{{ content }}` |
| HTML Pages with Front Matter | All `.html` pages     | Keep file extension, just add layout metadata  |

Each content page (e.g., `web_about_us.html`) will have a front matter block like this:

```html
---
layout: default
title: About Us
---
