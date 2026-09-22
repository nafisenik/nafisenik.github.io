---
layout: post
title: How I built this website with an AI agent
date: 2026-09-22 10:00:00+0200
description: Setting up an academic website with al-folio and a coding agent turned out to be surprisingly painless. Here is what actually worked.
tags: website al-folio agents
categories: meta
giscus_comments: false
related_posts: false
---

I always meant to build a proper academic website, and I always found a reason not to. Picking a template, adding publications, fixing the local build. It never felt worth an afternoon. This time I did it differently. I handed most of the work to a coding agent and told it what I wanted. A couple of hours later, the site was done.

Here is the short version, in case it saves someone else the same afternoon.

## The pieces

- **[al-folio](https://github.com/alshedivat/al-folio)** is a popular Jekyll theme for academics. Publications, news, CV, projects, and a blog all come built in. You mostly fill in content instead of writing HTML.
- **A coding agent.** I used one that can read my files, edit them, run commands, and search the web. The key part is that it sees the whole repository at once, so it understands how the template fits together.

## What I actually told the agent

I did not write a spec. I pointed it at the repo and my CV and described the goal in plain words. The prompts that did most of the work were roughly:

1. **"This is my personal webpage. Read the whole repo, then fill it with my real information — here is my CV, and here is my Google Scholar. Newest first. Don't change the layout much."** This swapped out all the placeholder content (the template is full of _Albert Einstein_ examples) for my bio, publications, education, teaching, and news.
2. **"Use this photo for the profile picture."** I pasted an image. It resized the image and put it in the right place.
3. **"The CI is failing — here is the log."** I pasted the red GitHub Actions output. It read the error, explained why (a CV-rendering action with a stricter schema than the site itself), and fixed it.
4. **"The blog has too many posts and isn't in the top menu. Clear it out, add it to the nav, and write one post about this."** That is the post you are reading.
