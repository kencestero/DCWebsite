# Diamond Cargo Website - Editing Guide

## Quick Start

### Before You Start Editing
```bash
git pull
```

### After Making Changes
```bash
git add .
git commit -m "Brief description of changes"
git push
```

## Recommended VS Code Extensions

When you open this project in VS Code, you'll see a notification to install recommended extensions. Click "Install All" or install them manually:

1. **Live Server** - Test changes in real-time in your browser
   - Right-click any HTML file → "Open with Live Server"
   - Your site will open at http://localhost:5501
   - Changes auto-refresh in browser!

2. **Auto Rename Tag** - Automatically rename paired HTML tags

3. **Prettier** - Format code automatically (formats on save)

4. **HTML CSS Support** - Better autocomplete for CSS classes

5. **CSS Peek** - Jump to CSS definitions

## Project Structure

```
diamond-logihub/
├── index.html              # Homepage
├── about.html              # About page
├── contact.html            # Contact page
├── dealers.html            # Custom: Dealers page
├── trailers.html           # Custom: Trailers page
├── options.html            # Custom: Options page
├── [other pages...]
└── assets/
    ├── css/                # Stylesheets (edit style.css)
    ├── js/                 # JavaScript files
    ├── img/                # Images
    ├── fonts/              # Icon fonts
    └── sass/               # SASS source files
```

## Common Editing Tasks

### 1. Update Site-Wide Content (Header/Footer/Navigation)

**Problem:** Changes need to appear on all 21+ pages

**Solution:** Use Find & Replace Across Files
- Press `Ctrl + Shift + H` (Windows) or `Cmd + Shift + H` (Mac)
- Click "..." → Include files → `*.html`
- Enter old text and new text
- Click "Replace All"

**Example:** Changing phone number across all pages

### 2. Update Contact Information

Current contact info locations:
- **Address:** "91 Harvey Vickers Rd, Douglas, GA 31535"
- **Email:** "Info@email.com" (placeholder - needs updating!)
- **Phone:** "+1-416-8241228"

To update:
1. Use Find & Replace across files: `Ctrl + Shift + H`
2. Include: `*.html`
3. Replace old value with new value

### 3. Change Images

**Best Practices:**
- Keep similar dimensions to originals
- Optimize images before adding (use tinypng.com or similar)
- Keep images under 500KB for fast loading
- Use descriptive alt text for SEO
- Place in `assets/img/` folder

**How to Replace:**
1. Add new image to `assets/img/`
2. Find old image path in HTML
3. Replace with new image path
4. Update alt text if needed

### 4. Update Styles/Colors

**Main CSS file:** `assets/css/style.css`

**Don't edit these:**
- `bootstrap.min.css`
- `swiper.min.css`
- Any `.min.css` files

**To customize:**
1. Open `assets/css/style.css`
2. Find the class you want to change
3. Update the styles
4. Save and refresh browser

## Git Workflow

### For Small Changes
```bash
git pull                           # Get latest changes
# Make your edits
git add .                          # Stage changes
git commit -m "Update pricing"     # Commit
git push                           # Push to GitHub
```

### For Major Changes (Recommended)
```bash
git checkout -b feature/new-design  # Create branch
# Make your edits
git add .
git commit -m "Redesign homepage"
git push -u origin feature/new-design
# Create Pull Request on GitHub
```

## Testing Checklist

Before committing changes:

- [ ] Test in browser with Live Server
- [ ] Check mobile view (F12 → Toggle device toolbar)
- [ ] Click all navigation links
- [ ] Test forms (if changed)
- [ ] Check multiple browsers (Chrome, Firefox, Safari)
- [ ] Validate HTML: https://validator.w3.org/

## Common Issues & Solutions

### Issue: Changes not showing
- **Solution:** Hard refresh browser (Ctrl + Shift + R)

### Issue: Broken layout after editing
- **Solution:** Check if you closed all HTML tags properly

### Issue: Git merge conflicts
- **Solution:** Always `git pull` before making changes

### Issue: Image not showing
- **Solution:**
  - Check file path is correct
  - Use relative paths: `assets/img/image.jpg` (not `C:\...`)
  - Check file extension matches (jpg vs jpeg)

## File References

When telling Claude what to edit, you can:

1. **Describe it:** "Change the phone number in the header"
2. **Right-click in browser dev tools:**
   - Right-click element → "Copy outerHTML"
   - Paste to Claude with description
3. **Show line number:** "index.html line 228"

## Important Reminders

✅ **DO:**
- Always pull before editing
- Test locally before committing
- Use descriptive commit messages
- Update all pages for header/footer changes
- Optimize images before adding

❌ **DON'T:**
- Edit directly on server
- Commit without testing
- Use absolute paths (C:\...)
- Add huge unoptimized images
- Edit .min.css or .min.js files

## Quick Commands

```bash
# Check what changed
git status

# See changes in detail
git diff

# Undo local changes (before commit)
git restore filename.html

# View commit history
git log --oneline

# Pull latest from GitHub
git pull

# Push to GitHub
git push
```

## Need Help?

- VS Code shortcuts: Press `F1` for command palette
- Git help: `git --help`
- HTML validation: https://validator.w3.org/
- CSS validation: https://jigsaw.w3.org/css-validator/

---

**Last Updated:** 2025-11-29
**Project:** Diamond Cargo Website
**Template:** LogiHub - Logistics & Transportation
