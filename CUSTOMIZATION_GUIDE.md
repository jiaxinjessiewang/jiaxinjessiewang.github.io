# Personalization Guide for Your Academic Pages Site

This guide provides concrete instructions on how to customize your site with your own content, images, and personal information.

## 📁 Files to Upload

### 1. Profile Images (Upload to `/images/` folder)

**Required:**
- **`profile.png`** or **`profile.jpg`** - Your main profile photo (recommended: 400x400px, square)
  - This appears in the left sidebar on every page
  - Format: PNG or JPG
  - Location: `/images/profile.png`

**Optional:**
- **`bio-photo.jpg`** - Alternative bio photo (recommended: 400x400px)
- **`bio-photo-2.jpg`** - Another alternative photo option

**How to upload:**
1. Take or find a professional headshot photo
2. Crop it to square (400x400px recommended)
3. In GitHub, navigate to the `images/` folder
4. Click "Upload files" button
5. Drag and drop your image file
6. Name it `profile.png` (or `profile.jpg`)
7. Commit the changes

### 2. Favicon Files (Upload to `/images/` folder)

**Required for professional appearance:**
- **`favicon.ico`** - 16x16 or 32x32px icon (appears in browser tab)
- **`favicon.svg`** - Scalable vector icon (modern browsers)
- **`favicon-32x32.png`** - 32x32px PNG version
- **`favicon-192x192.png`** - 192x192px PNG version (for Android)
- **`favicon-512x512.png`** - 512x512px PNG version (for iOS)
- **`apple-touch-icon-180x180.png`** - 180x180px for iOS home screen

**How to create:**
- Use an online favicon generator like [favicon.io](https://favicon.io/) or [realfavicongenerator.net](https://realfavicongenerator.net/)
- Upload a square image (your logo, initials, or photo)
- Download all generated sizes
- Upload them to `/images/` folder

### 3. PDF Files (Upload to `/files/` folder)

**For Publications:**
- Upload your research papers as PDFs
- Example: `paper1.pdf`, `paper2.pdf`
- These will be accessible at: `https://yourusername.github.io/files/paper1.pdf`

**For Talks:**
- Upload presentation slides as PDFs
- Example: `slides1.pdf`, `slides2.pdf`

**For CV:**
- Upload your full CV/resume as PDF
- Example: `cv.pdf` or `resume.pdf`

**How to upload:**
1. Navigate to the `files/` folder in GitHub
2. Click "Upload files"
3. Drag and drop your PDF files
4. Commit the changes

### 4. Social Media Preview Image (Optional)

- **`og-image.jpg`** or **`og-image.png`** - Image that appears when your site is shared on social media
  - Recommended size: 1200x630px
  - Upload to `/images/` folder
  - Then update `_config.yml` to reference it (see Configuration section below)

---

## ⚙️ Configuration Files to Edit

### 1. Main Configuration: `_config.yml`

**Location:** Root directory of your repository

**Key sections to update:**

#### Basic Site Settings (Lines 10-18)
```yaml
title: "Your Name / Site Title"  # Change to your name
name: "Your Name"                 # Your full name
description: "Your Name's academic portfolio"  # Brief description
url: https://yourusername.github.io  # Your GitHub Pages URL
baseurl: ""  # Leave blank unless site is in a subdirectory
repository: "yourusername/yourusername.github.io"  # Your repo name
```

#### Author Information (Lines 24-83)
```yaml
author:
  avatar: "profile.png"  # Your profile image filename
  name: "Your Sidebar Name"  # Name shown in sidebar
  pronouns: "she/her"  # Optional: your pronouns
  bio: "Short biography for the left-hand sidebar"  # 1-2 sentences about you
  location: "City, Country"  # Your location
  employer: "Your University/Company"  # Where you work/study
  email: "your.email@example.com"  # Your email
  
  # Academic profiles (add your URLs)
  googlescholar: "https://scholar.google.com/citations?user=YOUR_ID"
  orcid: "https://orcid.org/YOUR_ORCID_ID"
  pubmed: "https://www.ncbi.nlm.nih.gov/pubmed/?term=your+name"
  
  # Social media (add your usernames/URLs)
  github: "yourusername"
  twitter: "yourusername"
  linkedin: "yourusername"
  instagram: "yourusername"
  youtube: "yourusername"
```

#### Site Theme (Line 11)
```yaml
site_theme: "default"  # Options: "default", "air", "sunrise", "mint", "dirt", "contrast"
```
Try different themes to see which you prefer!

#### Social Media Preview (Lines 145-147)
```yaml
og_image: "og-image.jpg"  # Your social media preview image
og_description: "Your site description for social sharing"
```

#### Analytics (Optional, Lines 157-160)
```yaml
analytics:
  provider: "google-analytics-4"  # Change from "false" if you want analytics
  google:
    tracking_id: "G-XXXXXXXXXX"  # Your Google Analytics ID
```

### 2. Navigation Menu: `_data/navigation.yml`

**Location:** `_data/navigation.yml`

**What to do:**
- Reorder menu items by moving entries up/down
- Remove sections you don't need (delete the entire entry)
- Add new sections if needed

**Example - Remove "Guide" and reorder:**
```yaml
main:
  - title: "About"
    url: /
    
  - title: "Publications"
    url: /publications/
    
  - title: "CV"
    url: /cv/
    
  - title: "Talks"
    url: /talks/
    
  - title: "Teaching"
    url: /teaching/
    
  - title: "Portfolio"
    url: /portfolio/
    
  - title: "Blog"
    url: /year-archive/
```

### 3. Homepage/About Page: `_pages/about.md`

**Location:** `_pages/about.md`

**What to do:**
1. Change the `title` in the front matter (line 3)
2. Replace the template text with your own introduction
3. Add sections about:
   - Your research interests
   - Your background
   - Your current work
   - How to contact you

**Example:**
```markdown
---
permalink: /
title: "Your Name - Research Scientist"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

Welcome! I'm a [your title] at [your institution], where I research [your field].

## Research Interests

My work focuses on [describe your research]. I'm particularly interested in [specific topics].

## Background

[Your educational background and career path]

## Current Work

[What you're working on now]

## Contact

Feel free to reach out via email or social media!
```

---

## 📝 Content to Add/Update

### 1. Publications (`_publications/` folder)

**For each publication, create a file like:** `YYYY-MM-DD-paper-title.md`

**Template:**
```markdown
---
title: "Your Paper Title"
authors: "Your Name, Co-author Name"
date: 2024-01-15
venue: "Journal Name or Conference Name"
paperurl: 'https://link-to-paper.com'
citation: 'Your Name et al., Journal Name, 2024'
---
```

**To add a PDF:**
- Upload PDF to `/files/` folder
- Reference it in the front matter:
```yaml
paperurl: '/files/your-paper.pdf'
```

### 2. Talks (`_talks/` folder)

**For each talk, create a file like:** `YYYY-MM-DD-talk-title.md`

**Template:**
```markdown
---
title: "Your Talk Title"
venue: "Conference Name, Location"
date: 2024-03-15
location: "City, Country"
---
```

**To add slides:**
- Upload PDF to `/files/` folder
- Reference it:
```yaml
slides: '/files/your-slides.pdf'
```

### 3. Teaching (`_teaching/` folder)

**For each course, create a file like:** `YYYY-semester-course-name.md`

**Template:**
```markdown
---
title: "Course Name"
venue: "University Name"
date: 2024-01-15
---
Course description and details here.
```

### 4. Portfolio (`_portfolio/` folder)

**For each project, create a file like:** `project-name.md`

**Template:**
```markdown
---
title: "Project Name"
date: 2024-01-15
header:
  image: "/images/project-image.jpg"
  teaser: "/images/project-thumbnail.jpg"
---
Description of your project here.
```

### 5. Blog Posts (`_posts/` folder)

**For each post, create a file like:** `YYYY-MM-DD-post-title.md`

**Template:**
```markdown
---
title: "Your Blog Post Title"
date: 2024-01-15
categories:
  - Category Name
tags:
  - Tag1
  - Tag2
---
Your blog post content here.
```

### 6. CV (`_pages/cv.md` or `_data/cv.json`)

**Option 1: Markdown CV** - Edit `_pages/cv.md`
- Write your CV in Markdown format
- Sections are automatically formatted

**Option 2: JSON CV** - Edit `_data/cv.json`
- Structured data format
- More automated but requires JSON knowledge

---

## 🎨 Visual Customization

### 1. Change Site Theme

In `_config.yml`, change:
```yaml
site_theme: "air"  # Try: default, air, sunrise, mint, dirt, contrast
```

### 2. Custom CSS (Advanced)

Create `/assets/css/main.scss` and add custom styles:
```scss
// Your custom styles here
```

### 3. Custom Header/Footer

- Edit `_includes/masthead.html` for header customization
- Edit `_includes/footer.html` for footer customization

---

## ✅ Quick Start Checklist

**Essential (Do First):**
- [ ] Upload `profile.png` to `/images/` folder
- [ ] Update `_config.yml` with your name, email, bio
- [ ] Update `_config.yml` with your social media links
- [ ] Update `_pages/about.md` with your introduction
- [ ] Update `_config.yml` with your GitHub Pages URL

**Important (Do Soon):**
- [ ] Upload favicon files to `/images/` folder
- [ ] Update `_data/navigation.yml` to customize menu
- [ ] Add your publications to `_publications/` folder
- [ ] Add your talks to `_talks/` folder
- [ ] Update or remove sample content

**Optional (Polish Later):**
- [ ] Add teaching courses to `_teaching/` folder
- [ ] Add portfolio projects to `_portfolio/` folder
- [ ] Write blog posts in `_posts/` folder
- [ ] Set up Google Analytics
- [ ] Create social media preview image
- [ ] Customize theme colors/styles

---

## 🔗 Useful Resources

- **Preview your site locally:** Follow instructions in `README.md`
- **Markdown guide:** Check `_pages/markdown.md` on your site
- **Theme documentation:** [Minimal Mistakes docs](https://mmistakes.github.io/minimal-mistakes/docs/configuration/)
- **Jekyll documentation:** [Jekyll docs](https://jekyllrb.com/docs/)

---

## 💡 Pro Tips

1. **Test locally first:** Use `bundle exec jekyll serve` to preview changes before pushing to GitHub
2. **Keep backups:** Your Markdown files are your content - keep them safe!
3. **Use consistent naming:** Follow the date format `YYYY-MM-DD` for all content files
4. **Optimize images:** Compress images before uploading to keep site fast
5. **Update regularly:** Keep your publications, talks, and bio current

---

## 🆘 Need Help?

- Check the [Academic Pages wiki](https://github.com/academicpages/academicpages.github.io/wiki)
- Ask questions on [GitHub Discussions](https://github.com/academicpages/academicpages.github.io/discussions)
- Review the [Minimal Mistakes theme docs](https://mmistakes.github.io/minimal-mistakes/docs/configuration/)

