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

I always meant to have a proper academic website, and I always found an excuse not to. Choosing a template, wiring up publications, fighting with the local build — it never felt worth an afternoon. This time I tried something different: I handed most of the work to a coding agent and just told it what I wanted. A couple of hours later, this site existed.

Here is the short version of how it went, in case it saves someone else the same afternoon.

## The pieces

- **[al-folio](https://github.com/alshedivat/al-folio)** — a clean, popular Jekyll theme built for academics. Publications, news, CV, projects, and a blog all come for free. You mostly fill in content instead of writing HTML.
- **A coding agent** — I used one that can read my files, edit them, run commands, and search the web. The important part is that it can see the whole repository at once, so it understands how the template fits together.

## What I actually told the agent

I did not write a spec. I pointed it at the repo and my CV and described the goal in plain language. The prompts that did the heavy lifting were roughly:

1. **"This is my personal webpage. Read the whole repo, then fill it with my real information — here is my CV, and here is my Google Scholar. Newest first. Don't change the layout much."** This replaced every bit of placeholder content (the template ships full of *Albert Einstein* examples) with my bio, publications, education, teaching, and news.
2. **"Use this photo for the profile picture."** I pasted an image; it resized it and dropped it in the right place.
3. **"The CI is failing — here is the log."** I pasted the red GitHub Actions output. It read the error, explained *why* (a CV-rendering action with a stricter schema than the site itself), and fixed it.
4. **"The blog has too many posts and isn't in the top menu. Clear it out, add it to the nav, and write one post about this."** That is the post you are reading.

## What made it easy

A few things stood out:

- **Let it read first.** The single most useful instruction was "read the whole repo before changing anything." al-folio has a lot of interconnected config, and an agent that understands the structure makes far better edits than one that guesses.
- **Give it ground truth.** My CV as a PDF and a link to Google Scholar were enough for it to get names, venues, and dates right. Where it was unsure, it searched the web and asked me to confirm a couple of details rather than inventing them.
- **Paste the errors.** When the build or CI complained, pasting the raw log was faster than describing the problem. The agent could diagnose it directly.
- **Small, clear asks.** "Newest first," "don't change the layout," "hide the lab-members page" — short, concrete instructions were easier to act on than one giant paragraph.

## The honest caveats

It is not magic. I still reviewed everything: dates, author lists, and which papers to mark as *selected*. The agent flagged the things it inferred so I could check them, which is exactly what you want. Treat it as a very fast, very literal collaborator — not an oracle.

If you have been putting off your own academic site: pick al-folio, open the repo with an agent, hand it your CV, and start describing what you want. That is genuinely most of the work.
