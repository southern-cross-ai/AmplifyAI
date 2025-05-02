# 📅 Meeting Record: Sprint 2 - Week 1

**Date:** April 10th, 2025  
**Time:** 1PM – 2PM  
**Location:** Online  

---

## 🎯 1. Meeting Objective  
Discuss how to prepare our current static website for migration to the Jekyll framework by understanding its layout structure and planning component organization without enforcing unnecessary modularization.

## 📋 2. Core Discussion Points

### A. Understanding Jekyll’s Structure  
- Jekyll allows us to create modular, reusable websites using a layout-based system.  
- Unlike traditional static sites where each HTML file is standalone, Jekyll encourages using layouts and front matter to simplify structure and maintenance.  

### B. Existing Site Review  
We reviewed our current HTML files:

#### ✅ Pages:
- `index.html`  
- `web_about_us.html`, `web_contact.html`, `web_products.html`  
- `web_AI_trail.html`, `web_sub_AI_trail.html`  
- `web_latest_news.html`, `latest_news.html`  
- `members.html`, `SampleUI.html`

#### ✅ Assets:
- `footer.html`: already extracted and reusable  
- `style.css`, `script.js`: used across the site  

We agreed that maintaining `.html` format is the most practical approach, and we’ll integrate Jekyll support by adding front matter to each file:

```html
layout: default
title: Page Title
```

## ✅ 3. Action Items  
- [x] Backup current site files
- [x] Finalize file mapping between old .html and new Jekyll components
- [x] Organize team responsibilities for refactoring and integration
- [x] Test rendering of .html pages using Jekyll layout system

## 🔄 4. Looking Ahead  
- In the next stage, we will begin refining page styles and cleaning up the Jekyll directory structure.  
- If the rendering and integration tests are successful, we will prepare to deploy the site to GitHub Pages for preview and validation.

---

**Prepared by**: Yuhang Chen  
**Date**: April 10th, 2025  
