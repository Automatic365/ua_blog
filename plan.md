Project Blueprint: Personal Homepage & Markdown Blog
Project Overview
I am building a personal homepage and blog. I have zero coding experience, so I am acting as the project manager. You (Claude) will handle all file creation, terminal commands, and coding.

Technology Stack

Framework: Astro (specifically chosen for its native Markdown routing)

Styling: Tailwind CSS (for quick, responsive design)

Content: Markdown (.md files)

Hosting & Deployment: GitHub repository triggering automatic deployments to Vercel.

Design System & Vibe

Clean, modern, and highly minimalist.

Fully responsive (must look great on mobile and desktop).

High readability for blog typography (generous line spacing, clear font hierarchy).

Core Features & Page Structure

Homepage (/)

Hero Section: A brief "About Me" introduction.

Recent Posts: A dynamic grid or list displaying the 3 most recently published blog posts (pulling title, date, and a brief excerpt).

Footer/Contact: Links to my social media profiles and an email contact.

Blog Index (/blog)

A chronological list of all published Markdown posts.

Individual Blog Posts (/blog/[slug])

Dynamic routing that turns any Markdown file dropped into the content folder into a fully formatted web page.

Workflow Requirements (For the User)

Adding a new post must be as simple as adding a new title.md file to a specific src/content/blog/ directory.

No database setup; everything must be static and file-based.

Execution Plan (Claude's Tasks)
Please execute this project step-by-step. Stop and ask for my confirmation after each phase is completed before moving to the next. Provide the exact terminal commands I need to run.

Phase 1: Initialization. Run the setup commands for an empty Astro project and integrate Tailwind CSS.

Phase 2: Layout & Base. Create the global layout component (navigation bar, footer, and main content wrapper).

Phase 3: Content Collections. Set up the Astro Content Collections API for the blog to ensure my Markdown files are properly validated and routed.

Phase 4: Page Building. Build the Homepage (pulling the recent posts) and the Blog Index page.

Phase 5: Post Template. Build the dynamic route layout for individual blog posts.

Phase 6: Deployment Prep. Ensure the build script is ready and provide instructions on how to initialize the Git repository so I can push to GitHub and connect to Vercel.