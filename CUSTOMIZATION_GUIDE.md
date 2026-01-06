# Personalization Guide for Your Academic Pages Site

This guide provides concrete instructions on how to customize your site with your own content, images, and personal information.

**✨ No coding experience required!** All changes can be made directly on GitHub's website - no need to install anything or use command line tools.

## 🚀 Quick Start

**New to GitHub?** Start here:
1. Read the **"How to Edit Files on GitHub"** section below to learn the basics
2. Then follow the **"Quick Start Checklist"** at the bottom of this guide

**Already familiar with GitHub?** Jump to:
- **Files to Upload** - What images and PDFs you need
- **Configuration Files** - What settings to change
- **Content to Add** - How to add publications, talks, etc.

---

## 📂 Site Directory Structure

**Understanding where everything is located:**

```
your-repository/
│
├── 📄 _config.yml                    ← MAIN SETTINGS FILE (edit this first!)
│   └── Site title, your name, bio, social links, theme
│
├── 📁 _pages/                        ← YOUR PAGES (landing page, CV, etc.)
│   ├── about.md                      ← 🏠 LANDING PAGE (homepage)
│   ├── cv.md                         ← Your CV page
│   ├── publications.html             ← Publications listing page
│   ├── talks.html                    ← Talks listing page
│   ├── teaching.html                 ← Teaching listing page
│   ├── portfolio.html                ← Portfolio listing page
│   └── 404.md                        ← 404 error page
│
├── 📁 _data/                         ← DATA FILES
│   ├── navigation.yml                ← Top menu navigation
│   ├── authors.yml                   ← Author information
│   └── cv.json                       ← CV data (alternative to cv.md)
│
├── 📁 _publications/                  ← YOUR PUBLICATIONS
│   └── YYYY-MM-DD-paper-title.md     ← One file per publication
│
├── 📁 _talks/                        ← YOUR TALKS/PRESENTATIONS
│   └── YYYY-MM-DD-talk-title.md      ← One file per talk
│
├── 📁 _teaching/                     ← YOUR COURSES
│   └── YYYY-semester-course.md       ← One file per course
│
├── 📁 _portfolio/                    ← YOUR PROJECTS
│   └── project-name.md               ← One file per project
│
├── 📁 _posts/                        ← YOUR BLOG POSTS
│   └── YYYY-MM-DD-post-title.md      ← One file per blog post
│
├── 📁 images/                        ← YOUR IMAGES
│   ├── profile.png                   ← 🖼️ Your profile photo (sidebar)
│   ├── bio-photo.jpg                 ← Alternative bio photo
│   ├── favicon.ico                    ← Site icon (browser tab)
│   ├── favicon.svg                    ← Site icon (modern browsers)
│   └── [other images]                 ← Any other images you upload
│
├── 📁 files/                         ← YOUR PDFs & DOCUMENTS
│   ├── paper1.pdf                    ← Research papers
│   ├── slides1.pdf                   ← Presentation slides
│   └── cv.pdf                        ← Full CV PDF
│
└── 📁 _includes/                     ← TEMPLATE FILES (usually don't edit)
    └── [various HTML files]           ← Site structure templates
```

### 🎯 Key File Locations

| What You Want to Change | File Location |
|------------------------|---------------|
| **Landing Page (Homepage)** | `_pages/about.md` |
| **Site Title & Your Name** | `_config.yml` (lines 12-14) |
| **Your Bio & Social Links** | `_config.yml` (lines 24-83) |
| **Top Menu Navigation** | `_data/navigation.yml` |
| **Your Profile Photo** | Upload to `images/profile.png` |
| **Add a Publication** | Create new file in `_publications/` |
| **Add a Talk** | Create new file in `_talks/` |
| **Add a Blog Post** | Create new file in `_posts/` |
| **Your CV Page** | `_pages/cv.md` |
| **Site Theme** | `_config.yml` (line 11) |

### 📝 File Naming Conventions

**Important:** Follow these naming patterns for files to work correctly:

- **Publications:** `YYYY-MM-DD-paper-title.md`
  - Example: `2024-01-15-machine-learning-research.md`
  
- **Talks:** `YYYY-MM-DD-talk-title.md`
  - Example: `2024-03-20-conference-presentation.md`
  
- **Blog Posts:** `YYYY-MM-DD-post-title.md`
  - Example: `2024-02-10-my-research-journey.md`
  
- **Teaching:** `YYYY-semester-course-name.md`
  - Example: `2024-spring-introduction-to-computer-science.md`

**Why the date format?** The date in the filename determines the order and date shown on your site.

### 🗂️ What Each Folder Does

- **`_pages/`** - Static pages like your homepage, CV, and listing pages
- **`_publications/`** - Individual publication pages (automatically listed on Publications page)
- **`_talks/`** - Individual talk pages (automatically listed on Talks page)
- **`_teaching/`** - Individual course pages (automatically listed on Teaching page)
- **`_portfolio/`** - Individual project pages (automatically listed on Portfolio page)
- **`_posts/`** - Blog posts (automatically listed on Blog page)
- **`images/`** - All images (profile photos, icons, project images)
- **`files/`** - PDFs and documents (papers, slides, CVs)
- **`_data/`** - Configuration data (navigation menu, author info)
- **`_includes/`** - Template files (usually don't need to edit)

### 💡 Quick Navigation Tips

- **To edit your homepage:** Go to `_pages/about.md`
- **To change your name/bio:** Go to `_config.yml` (root directory)
- **To add content:** Create new files in the appropriate folder (`_publications/`, `_talks/`, etc.)
- **To upload images:** Go to `images/` folder → Click "Upload files"
- **To upload PDFs:** Go to `files/` folder → Click "Upload files"

---

## 🖥️ How to Edit Files on GitHub (Web Interface)

**You don't need to use an IDE or command line!** You can make all changes directly on GitHub's website. This section shows you exactly how.

### Navigating Your Repository

1. **Go to your repository:** Visit `https://github.com/yourusername/yourusername.github.io`
2. **Browse folders:** Click on folder names (like `_pages`, `images`, `_config.yml`) to navigate
3. **View files:** Click on any file name to view its contents
4. **Go back:** Use the breadcrumb navigation at the top or click the repository name

### Editing Existing Files

**Step-by-step instructions:**

1. **Navigate to the file you want to edit**
   - For example, to edit `_config.yml`, click on it in the root directory
   - To edit `_pages/about.md`, first click the `_pages` folder, then click `about.md`

2. **Open the file editor**
   - Once viewing the file, look for the **pencil icon** (✏️) in the top-right corner of the file view
   - It's located to the right of the "Raw | Blame | History" buttons
   - Click the pencil icon to enter edit mode

3. **Make your changes**
   - The file will open in GitHub's built-in editor
   - You can now edit the text, YAML, or Markdown content
   - The editor supports syntax highlighting for different file types

4. **Preview your changes (for Markdown files)**
   - If editing a `.md` file, click the "Preview" tab above the editor
   - This shows how your Markdown will render on the website

5. **Commit your changes**
   - Scroll down to the "Commit changes" section at the bottom of the page
   - In the "Commit message" box, write a brief description of what you changed
     - Example: "Update bio and email in config"
     - Example: "Add my profile photo information"
   - Choose "Commit directly to the `master` branch" (or `main` branch if that's your default)
   - Click the green **"Commit changes"** button

6. **Wait for GitHub Pages to rebuild**
   - GitHub Pages automatically rebuilds your site when you commit changes
   - This usually takes 1-3 minutes
   - You can check the status in your repository's "Actions" tab

### Uploading Files (Images, PDFs, etc.)

**For images, PDFs, and other binary files:**

1. **Navigate to the target folder**
   - For profile images: Go to the `images/` folder
   - For PDFs: Go to the `files/` folder
   - Click on the folder name to open it

2. **Click "Add file" button**
   - At the top of the folder view, you'll see an "Add file" button
   - Click the dropdown arrow next to it
   - Select **"Upload files"**

3. **Upload your file**
   - You can either:
     - **Drag and drop** files from your computer into the upload area
     - **Click "choose your files"** to browse and select files
   - You can upload multiple files at once

4. **Commit the upload**
   - Scroll down to the "Commit changes" section
   - Add a commit message like "Add profile photo" or "Upload paper PDFs"
   - Click **"Commit changes"**

**Important notes:**
- Make sure to name your files correctly (e.g., `profile.png` not `IMG_1234.jpg`)
- If uploading a file with the same name as an existing file, it will replace the old one
- Large files (>100MB) may not upload through the web interface

### Creating New Files

**For Markdown files, YAML files, and other text files:**

1. **Navigate to the folder where you want the new file**
   - For publications: Go to `_publications/` folder
   - For talks: Go to `_talks/` folder
   - For blog posts: Go to `_posts/` folder
   - For pages: Go to `_pages/` folder

2. **Click "Add file" button**
   - Click the "Add file" button at the top
   - Select **"Create new file"**

3. **Name your file**
   - In the "Name your file..." box at the top, enter the filename
   - **Important:** Use the correct naming format:
     - Publications: `YYYY-MM-DD-paper-title.md`
     - Talks: `YYYY-MM-DD-talk-title.md`
     - Blog posts: `YYYY-MM-DD-post-title.md`
   - Example: `2024-01-15-my-research-paper.md`

4. **Add content**
   - Type or paste your content into the editor
   - For Markdown files, include the front matter (YAML header) at the top
   - Use the templates provided in this guide

5. **Commit the new file**
   - Scroll down to "Commit changes"
   - Add a commit message like "Add new publication" or "Create about page"
   - Click **"Commit changes"**

### Deleting Files

1. **Navigate to the file you want to delete**
   - Click on the file to view it

2. **Click the trash icon**
   - Look for the **trash can icon** (🗑️) next to the pencil icon
   - It's in the top-right corner of the file view
   - Click it

3. **Confirm deletion**
   - Scroll down to "Commit changes"
   - Add a commit message like "Remove sample content"
   - Click **"Commit changes"**

**Note:** Be careful when deleting files! Make sure you don't need them anymore.

### Renaming Files

1. **Navigate to the file**
2. **Click the pencil icon to edit**
3. **Change the filename** in the "Edit file" box at the top
4. **Commit the change**

**Alternative method:**
- Delete the old file
- Create a new file with the new name
- Copy content from the old file (if you still have it)

### Viewing File History

**To see previous versions of a file:**

1. **Open the file**
2. **Click "History"** button (next to "Raw | Blame")
3. **Click on any commit** to see what changed
4. **Click "Browse files"** at that commit to restore an old version if needed

### Tips for Editing on GitHub

- **Save your work frequently:** Each commit is a save point
- **Use descriptive commit messages:** They help you track what changed and when
- **Preview Markdown:** Always use the Preview tab for `.md` files before committing
- **Check for syntax errors:** YAML files (like `_config.yml`) are sensitive to indentation and formatting
- **Test changes:** After committing, wait a few minutes and visit your site to see the changes
- **Use the search:** Press `/` while viewing your repository to quickly search for files

### Common GitHub Interface Elements

- **✏️ Pencil icon** = Edit file
- **🗑️ Trash icon** = Delete file
- **📁 Folder icon** = Navigate into folder
- **⬆️ Upload icon** = Upload files
- **➕ Add file** = Create new file or upload files
- **💬 Raw | Blame | History** = View raw file, see who changed what, view history
- **🔍 Search box** = Search files and code in repository

### Troubleshooting GitHub Web Editor

**Problem: Changes aren't showing on my site**
- Wait 2-3 minutes for GitHub Pages to rebuild
- Check the "Actions" tab in your repository for build errors
- Make sure you committed to the correct branch (usually `master` or `main`)

**Problem: Can't see the pencil icon**
- Make sure you're logged into GitHub
- Make sure you have write access to the repository
- Try refreshing the page

**Problem: File upload failed**
- Check file size (should be under 100MB)
- Try a different browser
- Make sure you have a stable internet connection

**Problem: YAML syntax errors**
- Check indentation (use spaces, not tabs)
- Make sure colons (`:`) have spaces after them
- Ensure quotes are properly closed
- Check the "Actions" tab for specific error messages

---

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

**How to upload (using GitHub web interface):**
1. Take or find a professional headshot photo
2. Crop it to square (400x400px recommended)
3. In GitHub, navigate to the `images/` folder (click on `images/` in your repository)
4. Click "Add file" → "Upload files"
5. Drag and drop your image file, or click "choose your files" to browse
6. Make sure the filename is `profile.png` (or `profile.jpg`) - rename it if needed
7. Scroll down and add a commit message like "Add profile photo"
8. Click "Commit changes"
9. Wait 2-3 minutes for your site to update

**See the "How to Edit Files on GitHub" section above for detailed step-by-step instructions with screenshots descriptions.**

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

**How to upload (using GitHub web interface):**
1. Navigate to the `files/` folder in GitHub (click on `files/` in your repository)
2. Click "Add file" → "Upload files"
3. Drag and drop your PDF files, or click "choose your files" to browse
4. You can upload multiple PDFs at once
5. Scroll down and add a commit message like "Add paper PDFs"
6. Click "Commit changes"
7. Wait 2-3 minutes for your site to update

**See the "How to Edit Files on GitHub" section above for detailed step-by-step instructions.**

### 4. Social Media Preview Image (Optional)

- **`og-image.jpg`** or **`og-image.png`** - Image that appears when your site is shared on social media
  - Recommended size: 1200x630px
  - Upload to `/images/` folder
  - Then update `_config.yml` to reference it (see Configuration section below)

---

## ⚙️ Configuration Files to Edit

### 1. Main Configuration: `_config.yml`

**Location:** Root directory of your repository

**How to edit on GitHub:**
1. Go to your repository homepage
2. Click on `_config.yml` (it's in the root directory, visible immediately)
3. Click the **pencil icon** (✏️) in the top-right corner
4. Make your edits in the editor
5. Scroll down, add a commit message like "Update site configuration"
6. Click "Commit changes"

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

**How to edit on GitHub:**
1. Click on the `_data` folder in your repository
2. Click on `navigation.yml`
3. Click the **pencil icon** (✏️) to edit
4. Make your changes
5. Commit with a message like "Update navigation menu"

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

**How to edit on GitHub:**
1. Click on the `_pages` folder in your repository
2. Click on `about.md`
3. Click the **pencil icon** (✏️) to edit
4. Use the "Preview" tab to see how your Markdown will look
5. Commit with a message like "Update about page"

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

**How to create on GitHub:**
1. Navigate to the `_publications/` folder (click on `_publications/`)
2. Click "Add file" → "Create new file"
3. Name the file: `YYYY-MM-DD-paper-title.md` (e.g., `2024-01-15-my-research.md`)
4. Copy the template below and fill in your information
5. Commit with a message like "Add new publication"

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

**How to create on GitHub:**
1. Navigate to the `_talks/` folder
2. Click "Add file" → "Create new file"
3. Name the file: `YYYY-MM-DD-talk-title.md`
4. Copy the template below and fill in your information
5. Commit with a message like "Add new talk"

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

**How to create on GitHub:**
1. Navigate to the `_teaching/` folder
2. Click "Add file" → "Create new file"
3. Name the file: `YYYY-semester-course-name.md` (e.g., `2024-spring-intro-to-cs.md`)
4. Copy the template below and fill in your information
5. Commit with a message like "Add teaching course"

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

**How to create on GitHub:**
1. Navigate to the `_portfolio/` folder
2. Click "Add file" → "Create new file"
3. Name the file: `project-name.md`
4. Copy the template below and fill in your information
5. Commit with a message like "Add portfolio project"

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

**How to create on GitHub:**
1. Navigate to the `_posts/` folder
2. Click "Add file" → "Create new file"
3. Name the file: `YYYY-MM-DD-post-title.md`
4. Copy the template below and fill in your information
5. Use the "Preview" tab to see how your post will look
6. Commit with a message like "Add new blog post"

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
- Navigate to `_pages/` folder → click `cv.md` → click pencil icon to edit
- Write your CV in Markdown format
- Sections are automatically formatted
- Use "Preview" tab to see formatting
- Commit with message "Update CV"

**Option 2: JSON CV** - Edit `_data/cv.json`
- Navigate to `_data/` folder → click `cv.json` → click pencil icon to edit
- Structured data format
- More automated but requires JSON knowledge
- Be careful with JSON syntax (commas, brackets, quotes)
- Commit with message "Update CV JSON"

### 7. Removing Sample Content

**Important:** The template comes with example files that you should remove or replace:

**Sample files to delete:**

1. **Sample blog posts** (`_posts/` folder):
   - Delete files like `2012-08-14-blog-post-1.md`, `2013-08-14-blog-post-2.md`, etc.
   - **How to delete:** Click on each file → Click trash icon → Commit deletion

2. **Sample publications** (`_publications/` folder):
   - Delete files like `2009-10-01-paper-title-number-1.md`, etc.
   - Replace with your own publications

3. **Sample talks** (`_talks/` folder):
   - Delete files like `2012-03-01-talk-1.md`, etc.
   - Replace with your own talks

4. **Sample portfolio** (`_portfolio/` folder):
   - Delete `portfolio-1.md`, `portfolio-2.html` if you don't need them
   - Or replace with your own projects

5. **Sample teaching** (`_teaching/` folder):
   - Delete sample teaching files if not applicable
   - Or replace with your own courses

**How to delete multiple files at once:**
- Unfortunately, GitHub web interface requires deleting files one at a time
- Alternatively, you can keep them as templates and edit them with your own content

**Tip:** Before deleting, you might want to copy the structure/template from sample files to use for your own content!

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
- [ ] Remove sample content (delete example files in `_posts/`, `_publications/`, `_talks/` folders)
  - **How to delete:** Click on a sample file → Click trash icon → Commit deletion

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

