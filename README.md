# Richie Lau Personal Website
A personal website built with `Jekyll` and hosted on `GitHub Pages`. This site explores the intersection of technology, music, and urban culture, and is customized using the Minima theme.

## Requirements
Before you start, make sure you have the following installed:

- Ruby
- Bundler

## Getting Started
1. **Clone the Repository**
```bash
git clone https://github.com/studiorichie/richielau.com.git
cd richielau.com
```

2. **Install Dependencies**
This will install Jekyll and any other dependencies listed in the `Gemfile`.

```bash
bundle install
```

## Local Development
To view the website locally while you make changes, run the following command:


```bash
bundle exec jekyll serve
```
By default, the site will be accessible at [http://127.0.0.1:4000].

## Quick Local Development Commands
- Start the local server: `bundle exec jekyll serve`
- Stop the server: `CTRL+C` in your terminal
- Clear the `_site` folder (optional): `rm -rf _site/` (useful if you encounter build issues)

# Deployment to GitHub Pages
GitHub Pages automatically rebuilds and deploys your site whenever changes are pushed to the repository. Here's the process:

1. **Stage and commit your changes**:

bash
Copy code
```bash
git add .
git commit -m "Your commit message here"
```
2. **Push to GitHub**:


```bash
git push origin main
```

After pushing, GitHub Pages should automatically publish your changes to your live site at https://richielau.com.

# Notes on Deployment
- Custom Domain: Make sure the `CNAME` file in the repository root contains your custom domain (e.g.,`richielau.com`).
Check GitHub Pages Status: It can take a few minutes for changes to be visible on the live site. To check if GitHub Pages is building your site, go to your repository on GitHub > Settings > Pages.

# Additional Resources
- Jekyll Documentation [https://jekyllrb.com/docs/]
- GitHub Pages Documentation[https://docs.github.com/en/pages]