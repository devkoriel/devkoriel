# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Purpose

This repository is for creating a GitHub profile README - the special README.md that appears on the user's GitHub profile page. This is created by making a repository with the same name as the GitHub username.

## GitHub Profile README Structure

A typical GitHub profile README includes:

1. **Header/Banner** - Eye-catching visual introduction
2. **About Me** - Brief introduction and current focus
3. **Skills & Technologies** - Tech stack, languages, tools
4. **Social Links** - Twitter, LinkedIn, personal website, etc.
5. **GitHub Stats** (optional) - Contribution stats, most used languages
6. **Contact Information** - Ways to reach out

## Common Tools & Services

### Badges and Shields
- [shields.io](https://shields.io/) - Generate badges for technologies, social media
- Format: `![Badge Label](https://img.shields.io/badge/...)`
- Use for: Languages, frameworks, tools, social media links

### Dynamic Content
- [github-readme-stats](https://github.com/anuraghazra/github-readme-stats) - GitHub statistics cards
- [github-readme-streak-stats](https://github.com/DenverCoder1/github-readme-streak-stats) - Contribution streak
- [github-profile-trophy](https://github.com/ryo-ma/github-profile-trophy) - Trophy display

### Assets Organization
```
/
├── README.md           # Main profile README
├── assets/            # Images, banners, icons
│   ├── banner.png
│   └── icons/
└── .github/
    └── workflows/     # GitHub Actions for dynamic updates (optional)
```

## Markdown Best Practices

### Alignment and Centering
```markdown
<div align="center">
  <img src="banner.png" />
  <h1>Your Name</h1>
</div>
```

### Social Media Links Pattern
```markdown
[![Twitter](https://img.shields.io/badge/Twitter-%231DA1F2.svg?logo=Twitter&logoColor=white)](https://twitter.com/username)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-%230077B5.svg?logo=linkedin&logoColor=white)](https://linkedin.com/in/username)
```

### Skills Section Pattern
```markdown
## 🛠️ Tech Stack

![Go](https://img.shields.io/badge/go-%2300ADD8.svg?style=for-the-badge&logo=go&logoColor=white)
![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![Kubernetes](https://img.shields.io/badge/kubernetes-%23326ce5.svg?style=for-the-badge&logo=kubernetes&logoColor=white)
```

## Preview and Testing

### Local Preview
1. View README.md in any Markdown preview tool
2. Use VS Code Markdown Preview (`Cmd+Shift+V` on macOS)
3. Push to GitHub and view on profile to see final rendering

### Validation
```bash
# Check for broken links (if using markdown-link-check)
npx markdown-link-check README.md

# Lint markdown (if using markdownlint)
npx markdownlint README.md
```

## Deployment

1. Repository name MUST match GitHub username exactly
2. README.md MUST be in root directory
3. Push to main branch - changes appear on profile immediately
4. GitHub caches profile READMEs, may take a few minutes to update

## Design Considerations

- **Mobile-friendly**: Many viewers will see this on mobile
- **Balanced content**: Not too sparse, not overwhelming
- **Working links**: All social media and website links should be functional
- **Updated information**: Keep current role, focus areas, and contact info fresh
- **Professional tone**: This is often a first impression for recruiters/collaborators
- **Accessibility**: Use alt text for images, semantic HTML when needed

## Common Sections to Include

**For DevOps/SRE Profile:**
- Current role and company
- Infrastructure expertise (Kubernetes, Terraform, etc.)
- Cloud platforms (AWS, GCP, Azure)
- Programming languages (Go, Python)
- Links to notable projects or contributions
- Blog or technical writing
- Open source contributions
- Contact and social media

## Git Workflow

```bash
# Initial setup
git init
git add README.md
git commit -m "feat: initial profile README"
git branch -M main
git remote add origin git@github.com:username/username.git
git push -u origin main

# Updates
git add README.md assets/
git commit -m "feat: update social links and tech stack"
git push
```

## Resources

- [awesome-github-profile-readme](https://github.com/abhisheknaiidu/awesome-github-profile-readme) - Inspiration and examples
- [Markdown Guide](https://www.markdownguide.org/) - Syntax reference
- [GitHub Profile README Generator](https://rahuldkjain.github.io/gh-profile-readme-generator/) - Quick start tool
