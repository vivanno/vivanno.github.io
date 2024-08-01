---
title: Install Jekyll on Ubuntu
layout: "post"
date: 2024-07-27T18:53:38.037Z
preview: ""
tags: [ubuntu, jekyll, ruby]
categories: [quick-start]
type: default
---

# What is Jekyll?
Jekyll is a static site generator that allows you to build and manage websites using plain text files and templates. It takes your content written in Markdown, Textile, or HTML, and generates a complete website that can be hosted on any web server. Jekyll is popular among developers for its simplicity, speed, and flexibility. It is often used for creating blogs, documentation sites, and personal websites.

# Install Ruby

```bash
$ sudo apt-get install ruby-full build-essential zlib1g-dev
```

# Set up Ruby Environment

```bash
$ echo '# Install Ruby Gems to ~/gems' >> ~/.bashrc
$ echo 'export GEM_HOME="$HOME/gems"' >> ~/.bashrc
$ echo 'export PATH="$HOME/gems/bin:$PATH"' >> ~/.bashrc
```
restart your terminal or run the following command: 

```bash
$ source ~/.bashrc
```

# Install Jekyll and Bundler

```bash
$ gem install jekyll bundler
```

# Create a new Jekyll site

```bash
$ jekyll new my-awesome-site
$ cd my-awesome-site
```

# Build the site and make it available on a local server

```bash
$ bundle exec jekyll serve
```

Now you can preview your site by browsing to [http://localhost:4000](http://localhost:4000)

Looking for a CMS? See [Front Matter CMS](https://frontmatter.codes/)