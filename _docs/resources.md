### Step 1: Install Jekyll
```
brew install ruby
gem install jekyll bundler
```

### Step 2: Create your site
```
jekyll new my_portfolio
cd my_portfolio
bundle exec jekyll serve
```

### Step 3: Things to know

1. Each file starts with front matter
2. Jekyll automatically turns this into a full HTML page with navigation, date and tags.
```
---
layout: post
title: "Building a RAG Pipeline with LangChain"
date: 2024-03-01
categories: [AI, LangChain]
tags: [RAG, vectors, embeddings]

## Introduction
Your blog content in **Markdown** starts here...
---
```
3. Structure files like this.
```
my-portfolio/
├── _config.yml       ← Site settings (name, bio, social links)
├── _posts/           ← Your blog posts go here
├── _layouts/         ← HTML templates
├── assets/           ← Images, CSS, JS
├── index.md          ← Homepage or main content
└── about.md          ← About page
```


