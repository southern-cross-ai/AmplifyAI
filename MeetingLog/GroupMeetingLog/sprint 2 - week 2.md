**📅 Meeting Record: Sprint 2 - Week 2**

**Date:** April 24th, 2025  
**Time:** 2–3 PM  
**Location:** Online  

---

## 🎯 1. Meeting Objective  
This week’s focus was on deploying our group’s website using **Jekyll**, and resolving related technical issues—especially on macOS environments.

---

## 📋 2. Core Discussion Points

### A. Learning & Practicing Jekyll Deployment  
- We followed a Bilibili tutorial to understand how to build and deploy a website using Jekyll. Key steps included:  
  1. Running the site locally with Jekyll for testing and previewing changes.  
  2. Pushing updates to a GitHub repository.  
  3. Using GitHub Pages for automated deployment.  

- We also discussed Jekyll’s folder structure, Markdown content management, and theme configuration, and drafted a basic collaboration workflow.

### B. macOS Environment Issue: Ruby Installation  
- One member encountered an issue when installing Jekyll on macOS due to the system’s outdated Ruby version (typically 2.6.10), resulting in errors such as:
  ```bash
  Gem::FilePermissionError: You don't have write permissions for the /Library/Ruby/Gems/... directory
  ```

- After referencing the [official Jekyll documentation](https://jekyllrb.com/docs/installation/macos/) and additional online guides, we learned that **it is not recommended to use system Ruby** on macOS for installing gems like Jekyll.

- We resolved the issue by setting up a modern Ruby environment using a version manager. Steps taken:
1. Install `chruby` and `ruby-install` using Homebrew:  
   ```bash
   brew install chruby ruby-install
   ```
2. Install the latest Ruby:  
   ```bash
   ruby-install ruby
   ```
3. Configure `.zshrc` or `.bashrc` to activate `chruby`, and switch to the new Ruby version.  
4. Install Jekyll and Bundler using the new Ruby environment:  
   ```bash
   gem install jekyll bundler
   ```

- The team resolved the issue collaboratively during the meeting and documented the solution for reference.

---

## ✅ 3. Action Items  
- [ ] **Environment Setup Guide**: Document macOS Ruby and Jekyll installation steps.  
- [ ] **Standardize Jekyll Workflow**: Finalize and share the local-to-GitHub Pages deployment procedure.  
- [ ] **Deployment Practice**: Each member should complete a Jekyll deployment test and submit feedback before the next meeting.

---

**Prepared by**: Yuhang Chen  
**Date**: April 24th, 2025  
