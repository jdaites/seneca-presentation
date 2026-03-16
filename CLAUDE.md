# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a single-file HTML slide presentation titled "From Broken Bottles to $4M Revenue/yr — Josh Daiter, InVintory." It is a self-contained `index.html` with all CSS and JavaScript inline.

## Running

Open `index.html` directly in a browser. No build step, bundler, or dev server is needed.

## Deploying

Hosted on GitHub Pages. To deploy changes:

```bash
git add -A && git commit -m "your message" && git push
```

Auto-deploys on push to `main`. Live at: https://jdaites.github.io/seneca-presentation/

## Architecture

- **index.html** — the entire presentation: styles, slides, and navigation logic in one file. Fonts and images reference local files in `assets/`.
- **assets/** — images (logos, screenshots, headshots) and trial font files (Canela Light/LightItalic OTF).

### Design system (CSS custom properties on `:root`)
- Gold brand palette: `--gold`, `--gold-dark`, `--gold-light`
- Dark backgrounds: `--dark` (#111), `--dark-card` (#1C1C1C)
- Text hierarchy: `--white`, `--text-secondary` (0.7 opacity), `--text-tertiary` (0.5 opacity)
- Slide variants via classes: `.slide-gradient`, `.slide-dark`, `.slide-gold`, `.center-content`
- Primary font: Lexend Deca (Google Fonts), accent font: Canela (embedded)

### Slide navigation (vanilla JS at bottom of file)
- Arrow keys, Space, PageDown/PageUp, Home/End for keyboard nav
- Touch swipe support (50px threshold)
- Progress bar + slide counter auto-update via `updateSlide()`
- Slides are `<div class="slide">` elements; the `.active` class controls visibility

## Presentation Content & Source Answers

The presentation was built from a Q&A interview with Josh Daiter, founder of InVintory. Below are the full answers used to generate the slides. Use these as the source of truth when editing slide content, adding slides, or adjusting messaging.

### The Origin Story

**The "aha moment":** Josh's dad is a wine collector and serial entrepreneur. After exiting his previous venture (selling medical clinics to PE), he wanted to retire, write screenplays, and collect wine. He tried Excel, Google, and found Cellar Tracker — the only real competitor, built 20-25 years ago and looking like Yellow Pages. In 2019 Josh saw a huge gap: no modern app existed for wine collection management. The wine market is bigger than books and music combined.

**The location feature origin:** Josh's dad was searching for a bottle, opening fridge shelves, and a bottle rolled off and smashed — red wine everywhere. That was the bottle he was looking for. That was the last straw: they needed a platform to manage AND locate bottles in a collection.

**Age/background when starting:** Started InVintory straight out of university. Caught the entrepreneurship bug earlier with a failed "skip the bar line" business (concept was right, execution wasn't — a big business does the same thing now). Went through the MMIE program (same one Bridget and Sundar did). Background was software engineering, fell in love with app development and delivering value.

**The angel investor story:** During MMIE end-of-year presentations, pitching to angels in Kingston, one guy laid into every company. After Josh's pitch he said "There's absolutely no way anyone is going to need this. I have a friend in China with a huge wine collection, and there's no way he needs this." Gave Josh 30 seconds after: "You seem like a smart guy. Your business is a waste of time. Go do something else." That lit a fire — Josh wanted to prove him wrong.

### The Journey

**Biggest early mistake — not trusting his gut:** Spent a ton of early investment dollars on initiatives that didn't work (e.g., hosting wine events — sounds logical for a wine tech company but was a money pit). Josh knew in his gut it wasn't the right strategy but wasn't fully in charge of marketing and didn't push back. When he took control of marketing, he executed on his instinct: InVintory is a tool, an app on the App Store — acquire users the way App Store users get acquired. Launched digital marketing campaigns and a content program. That became the main growth engine and let them understand unit economics.

**Key advice on unit economics:** Understand your unit economics early. Have a plan for product pricing, then figure out what you need to spend to acquire a customer. If you're spending $1,000 to acquire a $10 customer, don't pursue it. Know where to spend for cost of acquisition. Students have an advantage being tapped into social media, TikTok, etc. The biggest cost was opportunity cost.

**Almost quit five times:** Things weren't working for a long time before they figured it out. Almost ran out of money early on — raised a bunch, built a team way too fast, revenues didn't pick up as expected, had to do a layoff (~7 people). Josh committed to never doing that again. Advice: do NOT hire a single person until you can afford it. Don't take investment dollars and hire a bunch of people — use that money for growth. Letting people go has long-term consequences.

**On spiraling:** Every challenge and loss of hope is a moment where you can quit. If you're spiraling, take a breather and problem-solve. There's always a way to pivot or find something to get excited about. The biggest thing holding you back is you — rewrite the narrative in your head and stay positive.

**What he was wrong about — crowdfunding from users:** Josh's dad suggested raising from their user base instead of going to VCs. Josh scoffed at it. They sent an email to users and got $20M pledged. Obviously not all convertible, but they raised their first round from users. Josh now firmly believes in bootstrapping and keeping ownership over VC funding.

**Features that flopped:** They release features constantly and many flop. That's the point — run a thousand tests a year, put out hypotheses, take what works and iterate. It's an iterative process toward the successful end state.

### What Worked

**Side project to real business:** No single moment, but a series of realizations. The second fundraising round with serious backers, forming a board, seeing stable unit economics and growth curves. Even today Josh questions if it's successful — Apple featured them as App of the Day and he still questions it. "You'll never feel like things are successful, and that's okay. Keep pushing through."

**Growth drivers to ~$2M ARR with 10K+ subscribers:** Digital marketing campaigns and content program (after pivoting away from events). Understanding and optimizing unit economics.

### For the Students

**What he wishes someone had told him:** You just have to start. Build something start to finish. Don't perfect it — release it. It's uncomfortable. Get feedback, get revenue, fail, have people tell you it sucks. Iterate. Your product can suck on day one, even year one. Keep perfecting it. Building a business is messy.

**Understand WHY you're building:** VC funding looks glamorous — the press releases, LinkedIn sharing, looking accomplished. Then Josh realized: is that the goal? After having a child, he realized he cares about making money and providing for his family, not recognition. VCs only help a certain type of business (ones likely to grow to massive valuations that absolutely need capital). InVintory wasn't one of those. He'd rather stay lean and own more of his business. Ownership is freedom and freedom is happiness. He slightly regrets not going fully bootstrapped and would do it differently next time.

**Hot take on startups vs. traditional career:** Unless you're investing traditional career earnings in appreciating assets, you likely can't achieve the financial freedom most dream of without starting a business. Building a business is hard — you learn about yourself, others, the good/bad/ugly — but it's one of the only ways to have uncapped earning potential.

**On AI/tech trends (Vincent AI, Claude Code):** Now more than ever you can keep the most ownership, do everything yourself, and deliver insane value. Claude Code, Lovable, v0 — these platforms keep getting better. Josh says this as an engineer who doesn't want to admit these tools could replace his job, but they're amazing for entrepreneurship. He's jealous of students getting a fresh slate with fewer roadblocks. Caution: using these tools with no knowledge WILL generate AI slop — bugs, jank, security issues. That's okay — use it to test your idea, generate revenue, then use revenue to contract out or hire someone to fix issues, or reinvest in growth.
