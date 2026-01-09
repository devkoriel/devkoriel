# Setup Guide for GitHub Profile README

## Important: Repository Naming

This repository **MUST** be named exactly `devkoriel` to appear on your GitHub profile.

### Steps to Deploy

1. **Rename this repository** (if not already named correctly):
   ```bash
   # On GitHub, go to Settings > General > Repository name
   # Change to: devkoriel
   ```

2. **Push to GitHub**:
   ```bash
   git add .
   git commit -m "feat: initial animated profile README"
   git branch -M main
   git remote add origin git@github.com:devkoriel/devkoriel.git
   git push -u origin main
   ```

3. **Enable GitHub Actions** (for the snake animation):
   - Go to repository Settings > Actions > General
   - Under "Workflow permissions", select "Read and write permissions"
   - Click "Save"

4. **Trigger the snake animation**:
   - Go to Actions tab in your repository
   - Click on "Generate Snake" workflow
   - Click "Run workflow" > "Run workflow"
   - Wait for it to complete (creates the `output` branch)

5. **View your profile**:
   - Navigate to `github.com/devkoriel`
   - Your animated README should now appear!

## Customization

### Change Color Theme
The current theme uses purple/violet (`A855F7`). To change:
- Edit `README.md`
- Find and replace color codes:
  - `A855F7` (purple) → your preferred hex color
  - `radical` → other themes: `tokyonight`, `dracula`, `monokai`, `gruvbox`, `nord`

### Update Technologies
Edit the **Tech Stack** section in `README.md` to add/remove badges.

Find more badges at: https://github.com/Ileriayo/markdown-badges

### Modify Typing Animation
Edit the typing animation text in the first `readme-typing-svg` URL:
```
lines=Line+1;Line+2;Line+3
```
Use `+` for spaces and `;` to separate lines.

## Troubleshooting

**Snake animation not showing?**
- Ensure the workflow ran successfully (check Actions tab)
- Verify the `output` branch exists
- Check that the image URL matches your username: `devkoriel`

**Stats not loading?**
- GitHub's API can be rate-limited
- Try adding `&cache_seconds=1800` to the stats URLs
- Or deploy your own instance: https://github.com/anuraghazra/github-readme-stats

**Profile not updating?**
- GitHub caches profile READMEs
- Try force refresh (Ctrl+Shift+R / Cmd+Shift+R)
- Can take 5-10 minutes to propagate

## Resources

- [awesome-github-profile-readme](https://github.com/abhisheknaiidu/awesome-github-profile-readme)
- [GitHub Readme Stats](https://github.com/anuraghazra/github-readme-stats)
- [Shields.io Badge Generator](https://shields.io/)
- [Markdown Badges Collection](https://github.com/Ileriayo/markdown-badges)
