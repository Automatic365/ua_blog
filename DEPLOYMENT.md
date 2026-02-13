# Deployment Instructions

Your blog is now ready to deploy! Follow these steps to get it live on Vercel.

## Prerequisites

- A GitHub account
- A Vercel account (free tier is perfect - sign up at https://vercel.com)

## Step 1: Create a GitHub Repository

1. Go to https://github.com/new
2. Repository name: Choose a name (e.g., `my-blog` or `personal-website`)
3. Description: (Optional) "My personal blog built with Astro"
4. Keep it **Public** (or Private if you prefer)
5. **DO NOT** initialize with README, .gitignore, or license (we already have these)
6. Click **"Create repository"**

## Step 2: Push Your Code to GitHub

GitHub will show you commands after creating the repo. Use these commands in your terminal:

```bash
# Navigate to your project directory
cd "/Users/jhanna/Repo/Unfair Advantage/blog"

# Add the remote repository (replace YOUR-USERNAME and YOUR-REPO with your details)
git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPO.git

# Push your code
git push -u origin main
```

**Example:**
```bash
git remote add origin https://github.com/johndoe/my-blog.git
git push -u origin main
```

You may be prompted to authenticate with GitHub. Follow the prompts to log in.

## Step 3: Deploy to Vercel

1. Go to https://vercel.com and sign in (or create a free account)
2. Click **"Add New..."** → **"Project"**
3. Click **"Import Git Repository"**
4. Find and select your GitHub repository
5. Vercel will **automatically detect** that it's an Astro project
6. Click **"Deploy"**

That's it! Vercel will:
- Automatically configure the build settings
- Build your site
- Deploy it to a live URL (e.g., `your-blog.vercel.app`)

## Step 4: Your Blog is Live!

Once deployment completes (usually 1-2 minutes), Vercel will give you:
- A live URL (e.g., `https://my-blog-abc123.vercel.app`)
- Automatic SSL certificate (HTTPS)
- Automatic deployments on every git push

## Adding New Blog Posts

To publish a new blog post:

1. Create a new `.md` file in `src/content/blog/`
2. Add frontmatter with title, description, and date:

```markdown
---
title: "My New Post"
description: "A brief description of the post"
pubDate: 2024-02-13
author: "Your Name"
tags: ["topic1", "topic2"]
---

# Your content here...
```

3. Commit and push:

```bash
git add src/content/blog/your-new-post.md
git commit -m "Add new blog post: My New Post"
git push
```

Vercel will automatically rebuild and deploy your updated blog!

## Customization

Before going live, you'll want to customize:

- **src/pages/index.astro** - Update "Your Name" and the hero text
- **src/components/Footer.astro** - Update social media links and your name
- **src/layouts/BaseLayout.astro** - Update the default meta description
- **Delete sample posts** - Remove the 3 sample posts in `src/content/blog/` and add your own

## Custom Domain (Optional)

To use your own domain:

1. Purchase a domain (from Namecheap, Google Domains, etc.)
2. In Vercel dashboard, go to your project → Settings → Domains
3. Add your custom domain
4. Follow Vercel's instructions to update your DNS records

## Troubleshooting

**Build fails?**
- Check the Vercel build logs for errors
- Test locally first: `npm run build`
- Ensure all markdown files have valid frontmatter

**Changes not showing?**
- Vercel deploys automatically, but it takes 1-2 minutes
- Check the "Deployments" tab in Vercel to see status

**Need help?**
- Astro docs: https://docs.astro.build
- Vercel docs: https://vercel.com/docs

---

Enjoy your new blog! 🚀
