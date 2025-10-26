# Yuekun (Alice) Chen - Academic Website

Personal academic website for Yuekun (Alice) Chen, showcasing research, publications, and professional experience in psychological science and sociology.

**🌐 Live Site:** [https://alicechen58.github.io](https://alicechen58.github.io)

## About

I'm a graduating senior at the University of California, Irvine, earning dual Bachelor of Arts degrees in Psychological Science (Cum Laude) and Sociology (Magna Cum Laude) with a cumulative GPA of 3.95/4.00.

My research focuses on:
- Trauma and resilience across diverse populations
- Post-traumatic stress disorder (PTSD) and treatment outcomes
- Mental health in high-stress occupations
- Cultural adaptation of mental health interventions
- Sleep patterns and circadian rhythms in trauma survivors

### Current Positions

- **Lab Manager & Research Coordinator** - Trauma and Resilience Lab, UC Irvine
- **Project Coordinator** - Silver Stress and Coping Lab, UC Irvine  
- **Junior Research Specialist** - Stress, Coping and Health in Context Lab, UC Irvine

## Site Structure

This site includes:
- **Publications** - Manuscripts in preparation and published works
- **Talks & Presentations** - Conference presentations and symposiums
- **Research** - Detailed lab experience and projects
- **Portfolio** - Showcase of major research projects
- **Awards** - Academic honors and research funding
- **Service** - Crisis counseling and mental health advocacy
- **CV** - Comprehensive curriculum vitae
- **Blog** - Updates and news

## Contact

- **Email:** [yuekunc1@uci.edu](mailto:yuekunc1@uci.edu)
- **LinkedIn:** [linkedin.com/in/yuekun-alice-chen](https://linkedin.com/in/yuekun-alice-chen)
- **GitHub:** [@alicechen58](https://github.com/alicechen58)

---

## Technical Documentation

### 🚀 Automatic Deployment

This site uses **GitHub Actions** for push-to-publish automation. Every commit to `master` automatically builds and deploys to GitHub Pages. See [.github/DEPLOYMENT.md](.github/DEPLOYMENT.md) for setup instructions and troubleshooting.

### Running Locally

When you are initially working on your website, it is very useful to be able to preview the changes locally before pushing them to GitHub. To work locally you will need to:

1. Clone the repository and made updates as detailed above.

### Using a different IDE
1. Make sure you have ruby-dev, bundler, and nodejs installed
    
    On most Linux distribution and [Windows Subsystem Linux](https://learn.microsoft.com/en-us/windows/wsl/about) the command is:
    ```bash
    sudo apt install ruby-dev ruby-bundler nodejs
    ```
    If you see error `Unable to locate package ruby-bundler`, `Unable to locate package nodejs `, run the following:
    ```bash
    sudo apt update && sudo apt upgrade -y
    ```
    then try run `sudo apt install ruby-dev ruby-bundler nodejs` again.

    On MacOS the commands are:
    ```bash
    brew install ruby
    brew install node
    gem install bundler
    ```
1. Run `bundle install` to install ruby dependencies. If you get errors, delete Gemfile.lock and try again.

    If you see file permission error like `Fetching bundler-2.6.3.gem ERROR:  While executing gem (Gem::FilePermissionError) You don't have write permissions for the /var/lib/gems/3.2.0 directory.` or `Bundler::PermissionError: There was an error while trying to write to /usr/local/bin.`
    Install Gems Locally (Recommended):
    ```bash
    bundle config set --local path 'vendor/bundle'
    ```
    then try run `bundle install` again. If succeeded, you should see a folder called `vendor` and `.bundle`.

1. Run `jekyll serve -l -H localhost` to generate the HTML and serve it from `localhost:4000` the local server will automatically rebuild and refresh the pages on change to Markdown (*.md) and HTML files, while changes to the core template and configuration (i.e., `_config.yml`) will require stoping and restarting Jekyll.
    You may also try `bundle exec jekyll serve -l -H localhost` to ensure jekyll to use specific dependencies on your own local machine.

If you are running on Linux it may be necessary to install some additional dependencies prior to being able to run locally: `sudo apt install build-essential gcc make`

## Using Docker

Working from a different OS, or just want to avoid installing dependencies? You can use the provided `Dockerfile` to build a container that will run the site for you if you have [Docker](https://www.docker.com/) installed.

You can build and execute the container by running the following command in the repository:

```bash
chmod -R 777 .
docker compose up
```

You should now be able to access the website from `localhost:4000`.

### Using the DevContainer in VS Code

If you are using [Visual Studio Code](https://code.visualstudio.com/) you can use the [Dev Container](https://code.visualstudio.com/docs/devcontainers/containers) that comes with this Repository. Normally VS Code detects that a development coontainer configuration is available and asks you if you want to use the container. If this doesn't happen you can manually start the container by **F1->DevContainer: Reopen in Container**. This restarts your VS Code in the container and automatically hosts your academic page locally on http://localhost:4000. All changes will be updated live to that page after a few seconds.

### Content Editing Guide

This site is built on Jekyll with the academicpages structure. Here's a quick reference for editing different sections:

#### Site-wide Settings

- **`_config.yml`** — Title, tagline, email, description, social links, collections, and other global options
- **`_data/navigation.yml`** — Top navigation menu labels and links

#### Home & Profile

- **`_pages/about.md`** — Bio, headshot image path, quick links to CV, email, and socials
- **`images/HeadShot.jpg`** — Profile photo displayed on site

#### Publications & Talks

- **`_publications/*.md`** — One file per publication/preprint/in-prep item
- **`_talks/*.md`** — One file per talk/poster presentation
- **`markdown_generator/`** — Optional scripts to auto-generate content from TSV

#### Research & Portfolio

- **`_pages/research.md`** — Overview of research experience
- **`_portfolio/*.md`** — Detailed project cards for each lab/research experience

#### Other Sections

- **`_teaching/*.md`** — Teaching and mentorship entries
- **`_posts/YYYY-MM-DD-title.md`** — Blog posts and news updates
- **`_pages/service.md`** — Service and leadership activities
- **`_pages/awards.md`** — Honors, awards, and certifications
- **`_pages/cv.md`** — Online CV (also provide PDF in `files/`)

#### Assets

- **`files/`** — PDFs (CV, papers, slides) and downloadable files
- **`images/`** — All images referenced across pages

---

## About This Site

This website is built using the [Academic Pages](https://github.com/academicpages/academicpages.github.io) Jekyll template, which is based on the [Minimal Mistakes](https://mmistakes.github.io/minimal-mistakes/) theme.

**Technology Stack:**
- **Framework:** Jekyll static site generator
- **Hosting:** GitHub Pages
- **Deployment:** GitHub Actions (automated)
- **Theme:** Academic Pages template

**License:** MIT License

---

<div align="center">

**Yuekun (Alice) Chen** • [yuekunc1@uci.edu](mailto:yuekunc1@uci.edu) • University of California, Irvine

*Last updated: October 2025*

</div>
