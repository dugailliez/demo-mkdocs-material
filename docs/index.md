# Learn Continuous Deployment With Static Site Generators

## 1. What is Continuous deployment

Continuous deployment can be thought of as an extension of [continuous integration](https://www.agilealliance.org/glossary/continuous-integration/), aiming at minimizing [lead time](https://www.agilealliance.org/glossary/lead-time/), the time elapsed between development writing one new line of code and this new code being used by live users, in production.

## 2. What is a static site generator ?

> The basic concept of a static site generator (aka static site engine) is simple: take dynamic content and data and generate static HTML/JavaScript/CSS files that can be deployed to the server. This idea isn't new.

See this source : https://www.oreilly.com/ideas/static-site-generators.

* There are numerous services, both free and paid, that offer the ability to add dynamic aspects into static pages.
* Static site files are delivered to the end user exactly as they are on the server.
* There is no server-side language.
* There is no database.
* Static sites are HTML, CSS, and JavaScript.
* Performance, Hosting, Security, Content versioning are benefits of Static Sites.


**Practice** : Learn about [MkDocs](http://www.mkdocs.org/) and [Material for MkDocs](http://squidfunk.github.io/mkdocs-material/).

* MkDocs is a fast, simple and downright gorgeous static site generator that's geared towards building project documentation. Documentation source files are written in Markdown, and configured with a single YAML configuration file.
* Material is a theme for MkDocs. It is built using [Google's Material Design guidelines](https://material.io/guidelines/material-design/).

**Practice :** See the [advantages and the disadvantages](https://www.quora.com/What-are-the-pros-and-cons-of-using-static-site-generators) of [static website generators](https://www.staticgen.com/).

**Practice :** You can choose so many projects using [static site generator](https://www.staticgen.com/).


## 3. Connect to GitHub

>Git is a version control system for tracking changes in computer files and coordinating work on those files among multiple people. It is primarily used for source code management in software development, but it can be used to keep track of changes in any set of files. As a distributed revision control system it is aimed at speed, data integrity, and support for distributed, non-linear workflows.

> Git was created by Linus Torvalds in 2005 for development of the Linux kernel, with other kernel developers contributing to its initial development.

>As with most other distributed version control systems, and unlike most client–server systems, every Git directory on every computer is a full-fledged repository with complete history and full version tracking abilities, independent of network access or a central server.

> Git is free software distributed under the terms of the GNU General Public License version 2.

Source : https://en.wikipedia.org/wiki/Git

**Practice :** [Learn Git](https://try.github.io/) and GitHub.

* Create a GitHub user account.
* Connect to Github.
* Install [`git`](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git) or [`GitHub Desktop`](https://help.github.com/desktop/guides/getting-started-with-github-desktop/installing-github-desktop/#platform-windows) localy.

## 4. Deploy this site with Netlify

**Practice :** [Learn what is Netlify (builds, deploys, and hosts websites in continous development mode)](https://www.netlify.com/docs/continuous-deployment/).

Netlify personal plan (free) features :

* Personal or commercial projects
* Public or private repositories
* HTTPS for custom domains
* Continuous Deployment
* Form handling (BETA)
* Community support
* Identity service (BETA)
* Split Testing (BETA)
* Git Gateway (BETA)

Source : https://www.netlify.com/pricing/

**Practice :** See what is a front end build tool like Grunt, Gulp or Broccoli.

* [Grunt](https://gruntjs.com/) : Why use a task runner?
In one word: automation. The less work you have to do when performing repetitive tasks like minification, compilation, unit testing, linting, etc, the easier your job becomes. After you've configured it through a Gruntfile, a task runner can do most of that mundane work for you—and your team—with basically zero effort.
* [Gulp](https://gulpjs.com/) : gulp is a toolkit for automating painful or time-consuming tasks in your development workflow, so you can stop messing around and build something.
* [Broccoli](https://github.com/broccolijs/broccoli) : A fast, reliable asset pipeline, supporting constant-time rebuilds and compact build definitions. Comparable to the Rails asset pipeline in scope, though it runs on Node and is backend-agnostic.

Here is the best part, [Deploy this site with Netlify.](https://app.netlify.com/start/deploy?repository=https://github.com/goffinet/demo-mkdocs-material)

* Choose a repository name, for example : `mysite-dev`
* Click on "Save and deploy".

**Practice :** discover the Netlify interface and features.

## 5. DNS Service and settings

**Practice :** Distinguish Domain Registrar service and DNS Service.

**Practice :** Review the [DNS concepts](https://en.wikipedia.org/wiki/Domain_Name_System).

**Practice :** Learn [what is cloudflare](https://blog.cloudflare.com/what-is-cloudflare/).

1. Get a domaine name (https://www.ovh.com/fr/domaines/) : for example, `example.com`
2. Choose Cloudflare NS IP addresses
* Choose a DNS service (https://www.cloudflare.com/)
* Create a CNAME `mysite mysite-dev.netlify.com`

## 6. Setup a custom domain

1. Go to "mysite/settings/general"
* Click on the button "Change site name" : for example `mysite`
* Go to "Settings/Somain management/Domains"
* Click on the button "Add a custom domain" : `mysite.example.com`

## 7. Secure your site with HTTPS

**Practice :** Review HTTPS security and certificates concepts.

**Practice :** Learn about [Let’s Encrypt](https://letsencrypt.org/about/). Let’s Encrypt is a free, automated, and open certificate authority (CA), run for the public’s benefit. It is a service provided by the [Internet Security Research Group (ISRG)](https://letsencrypt.org/isrg/).

Let’s Encrypt gives people the digital certificates they need in order to enable HTTPS (SSL/TLS) for websites, for free, in the most user-friendly way we can. We do this because we want to create a more secure and privacy-respecting Web.

1. Go to Settings/Domain management/HTTPS
* Verify DNS is configured correctly before enabling HTTPS : click on the button "Verify DNS Configuration".
* Provision a certificate for your domain and enable HTTPS : click on the button "provision a certificate for your domain and enable HTTPS".
* Click on "Force HTTPS" after the certificate generation.

## 8. Customize your site

**Practice :** Review git with or with .

**Practice :** Learn the Markdown Language : Markdown is essentially a syntax for a simple, easy-to-read, plain text format that is designed to be converted to HTML ([source](https://www.oreilly.com/ideas/static-site-generators)). Most blog engines have started offering support for Markdown, including Wordpress.

**Practice :** Install localy a web-development tools offer Markdown support out of the box, including [Sublime Text](http://www.sublimetext.com/), [Atom](https://atom.io/), [Visual Studio Code](https://code.visualstudio.com/), or [Brackets](http://brackets.io/).

* Clone localy the repository `https://github.com/myaccount/mysite-dev/`.
* Add some content pages  written in Markdown into the `docs/` directory.
* Configure the `mkdocs.yml` file and adat the summary part.
* Commit and push your new code with `git`.

```bash
git clone https://github.com/myaccount/mysite-dev/
cd mysite-dev
vi docs/index.md
vi mkdocs.yml
git add *
git commit -m "site customization"
git push
```

## 9. Suggested actions

* Create a [Google Analytics](https://analytics.google.com/) a site with a following ID.
* Create a site in your [disqus account](https://disqus.com/admin/).
* Register the site to [Google Search console](https://www.google.com/webmasters/tools/home?hl=fr&pli=1) and launch the site indexation.

## 10. Other projects

### 10.1. Pure static site

* Pure static website : clone [this site](https://github.com/goffinet/crackciscotype7password) and/or [netlify it](https://app.netlify.com/start/deploy?repository=https://github.com/goffinet/crackciscotype7password) without any build command.

### 10.2. Gitbook

What is Gitbook ?

>GitBook is a command line tool (and Node.js library) for building beautiful books using GitHub/Git and Markdown (or AsciiDoc). Here is an example: [Learn Javascript](https://www.gitbook.com/book/GitBookIO/javascript).

>You can publish and host books easily online using [gitbook.com](https://www.gitbook.com). A desktop editor is [also available](https://www.gitbook.com/editor).

>Check out the [GitBook Community Slack Channel](https://slack.gitbook.com), Stay updated by following [@GitBookIO](https://twitter.com/GitBookIO) on Twitter or [GitBook](https://www.facebook.com/gitbookcom) on Facebook.

>Complete documentation is available at [toolchain.gitbook.com](http://toolchain.gitbook.com/).

* [Netlify this](https://app.netlify.com/start/deploy?repository=https://github.com/goffinet/gitbooktest) gitbook projects

Source : https://github.com/GitbookIO/gitbook

### 10.3. Netlify-CMS

What is Netlify-CMS ?

>Netlify CMS is a Content Management System for static sites, allowing collaborators to create, edit, review, and publish content without writing code or dealing with version control. It brings the ease of WordPress-style editing to the simplicity and speed of static sites.

>At its core, Netlify CMS is an open-source React app that acts as a wrapper for the Git workflow, using the GitHub API. This provides many advantages, including:

>Fast, web-based UI: with rich-text editing, real-time preview, and drag-and-drop media uploads.

>* Platform agnostic: works with most static site generators.
>* Easy installation: add two files to your site and hook up the backend by including in your build process or linking to our CDN.
>* Modern authentication: using GitHub and JSON web tokens.
>* Flexible content types: specify an unlimited number of content types with custom fields.
>* Fully extensible: create custom-styled previews, UI widgets, and editor plugins.

Source : https://www.netlifycms.org/docs/intro/

* Netlify [this project](https://app.netlify.com/start/deploy?repository=https://github.com/netlify-templates/one-click-hugo-cms&stack=cms) Netlify-CMS

### 10.4. Hosting sites with gh-pages

* Hosting with GitHub Pages : https://pages.github.com/