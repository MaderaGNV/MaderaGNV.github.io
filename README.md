
# MaderaGNV.github.io

<!-- badges: start -->
<!-- badges: end -->

This GitHub repository sets up the website for the Madera Community Association, which can be found at https://maderagnv.github.io/ .

## Contributions

If you are requesting maintainer access, please contact the administrators of the [MaderaGNV GitHub Organization Account](https://github.com/orgs/MaderaGNV/people) to be added to the maintainer team.

## Website Content

The website is built using [Hugo](https://gohugo.io/) as the static site generator and the [Hugo Scroll](https://themes.gohugo.io/themes/hugo-scroll/) theme.

To change the contents of pages, generally add or edit the markdown (`*.md`) files in the `content` folder.
  For the necessary structure of the files, it is recommended to look at existing files in this repository.
  For a quick guide to markdown syntax for formatting, see [this GitHub guide](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/quickstart-for-writing-on-github).

### Madera Community Association (MCA) documents

Existing MCA documents have been uploaded in both MS Word (`*.docx`) format and as viewable webpages.

1. The webpages are located in `content/docs` and formatted using markdown.

2. The MS Word versions are located in the `static/docs` directory.

3. Additionally, a link should be added to `content/homepage/documents.md` for the webpage version in 1. The links to the download versions are automatic 
In `content/homepage/documents.md` there is a "shortcode" that looks like:
```
{{< docs >}}
```

This runs the code in `layouts/shortcodes/docs.html` to look for files ending in `.docx` in the above specified location and generates a link.

## Website Deploy Logistics

The contents of the website are determined by the files in this repository.

When changes are made to the files (in the `main` branch of the repository), a [GitHub Actions script](https://github.com/MaderaGNV/MaderaGNV.github.io/blob/main/.github/workflows/blogdown.yaml) will run that re-renders the static site, pushes the contents of the new static site to the `gh-pages` branch of the repository, and then GitHub serves the content from there to the https://maderagnv.github.io/ destination.

