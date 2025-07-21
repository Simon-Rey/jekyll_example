# Example Jekyll Project

This is a simple starter project for building static websites using [Jekyll](https://jekyllrb.com/). It includes examples of layouts, pages, data usage, and GitHub Actions deployment.

See the deployed webiste [here](https://simon-rey.github.io/jekyll_example/).

---

## Getting Started

### 1. Install Jekyll

Follow the official installation guide: [https://jekyllrb.com/docs/installation/](https://jekyllrb.com/docs/installation/)

Make sure you have **Ruby**, **Bundler**, and **Jekyll** installed.

### 2. Run Locally

```bash
bundle install
bundle exec jekyll serve
```

Then visit [http://localhost:4000](http://localhost:4000) in your browser.

---

## Project Structure

| Folder/File            | Purpose                                                                                                                                                                                 |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `_layouts/`            | Defines the structure for different types of pages (e.g., `page`, `post`, `home`). Each page uses a layout defined in its YAML front matter (`layout: page`).                           |
| `*.md`                 | Markdown content pages. Pages are rendered using the assigned layout and can include [Liquid](https://shopify.github.io/liquid/) templating. Pages can also be described as HTML files. |
| `_data/`               | Stores reusable data in YAML/JSON/CSV files. You can reference this data in your pages or layouts using Liquid.                                                                         |
| `assets/`              | Contains static files like CSS, JavaScript, and images. These are copied over during site build.                                                                                        |
| `.github/workflows/`   | Contains GitHub Actions workflow for automated deployment.                                                                                                                              |

---

## Example Features

- `team.md` shows how to render a page using external data from `_data/team_data.yml`.
- Layouts make it easy to maintain consistent page design.
- Easily extendable to support blogs, portfolios, documentation sites, and more.
- You can use includes to include pieces of code in several locations.

---

## Deployment with GitHub Actions

This project is configured to deploy automatically using GitHub Actions.

- See the workflow in `.github/workflows/build_jekyll.yml`
- No manual setup is required — just **push your changes**, and the site is rebuilt automatically.
- Make sure GitHub Actions are enabled for your repository.
- In the settings -> Page, for source choose 'GitHub Action'
- If you want to deploy with a custom domain name, then the action needs to be updated (remove the --baseurl argument in the action)

---

## Notes

- Layouts are defined in the `_layouts` folder.
- Pages declare their layout in the YAML front matter: `layout: page`, `layout: default`, etc.
- Data used across pages (like team members or product info) lives in the `_data` folder.
- Static files like images, CSS, and JavaScript go in the `assets` folder.

---
