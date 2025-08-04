
Markdown

# HOFAMSCO School Website – Git Branching Guide

## 🔰 1. Create the dev Branch from main
```bash
# Switch to main branch
git checkout main

# Pull the latest changes from remote
git pull origin main

# Create dev branch off main
git checkout -b dev

# Push dev branch to remote
git push -u origin dev
🔹 The -u flag sets origin/dev as the default upstream for easy future pushes.

✨ 2. Create a Feature Branch (e.g., feature/header) from dev
Bash

# Make sure you're on dev
git checkout dev
git pull origin dev

# Create feature branch
git checkout -b feature/header

# Push the new feature branch
git push -u origin feature/header
🔁 3. Switch Between Branches
Bash

# To switch to dev
git checkout dev

# To switch to main
git checkout main

# To switch to a feature branch
git checkout feature/header
💾 4. Save and Commit Your Changes
Bash

# Stage your changes
git add .

# Commit with a clear message
git commit -m "Add responsive header component"

# Push to the remote feature branch
git push
🔀 5. Merge Feature Branch Into dev
Bash

# Switch to dev
git checkout dev

# Pull latest just to be safe
git pull origin dev

# Merge the feature branch
git merge feature/header

# Push updated dev
git push
🚀 6. Merge dev into main for Production
Only do this when everything is tested and confirmed working.

Bash

# Switch to main
git checkout main
git pull origin main

# Merge dev into main
git merge dev

# Push updated main branch
git push
🧹 7. Clean Up Merged Branches
Bash

# Delete the local branch
git branch -d feature/header

# Delete the remote branch
git push origin --delete feature/header
✅ Branch Naming Guidelines
Branch Type	Format Example	Use Case
Main Branch	main	Stable production version
Development	dev	Active staging and testing base
Feature	feature/section-name	New page sections, components
Fix	fix/what-you-fixed	Bug fixes, patch updates
Style	style/ui-update	UI layout or Tailwind tweaks
SEO	seo/meta-update	Metadata, OG tags, structured data
