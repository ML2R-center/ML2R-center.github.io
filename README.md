# [ml2r-center.github.io](https://ml2r-center.github.io/)

GitHub pages featuring ML2R-affiliated software repositories.

## Adding content

Adding an entry to `_data/software.yml` will publish your software on the GitHub page. You can [edit this file online](https://github.com/ML2R-center/ML2R-center.github.io/edit/main/_data/software.yml).

```yaml
- name: title of the supplemented paper OR name of the library
  type: "e" OR "l" (see below)
  url: where to link (ONLY PUBLIC REPOSITORIES)
  description: paper authors and venue OR sentence about the library
  areas: [ "h", "r", "t", "q", "o" ] (see below)
  biburl: optional URL of a corresponding BibTeX reference
  keywords: [ "optional", "keywords", "that are not redundant with the description" ]
```

- The shortcuts in `type` and `areas` will display colored badges (see the table below).
- All of the content (name, type, areas, description, keywords) can be used to search for entries.
- The BibTeX URL is optional; remove the field if not applicable.
- Only use keywords that do not appear in the rest of your entry.
- When a change is pushed to the `main` branch, GitHub pages will re-build the website immediately.

shortcut | resulting badge
-------- | -------
e        | type:experiment
l        | type:library
h        | area:hybrid
r        | area:resource-aware
t        | area:trustworthy
q        | area:quantum
o        | area:other

**BibTeX:** Any persistent(!) URL to a BibTeX entry will work, e.g. via Google Scholar or via DBLP. On DBLP, you can navigate to your publication and click on the download button, which should give you a URL that ends with `?view=bibtex`:

```
https://dblp.uni-trier.de/rec/journals/ki/Wrobel97.html?view=bibtex
```


## Need help?

Instead of pushing to the `main` branch directly, feel free to open a pull request and let someone check your entries.


## Feature requests

Please use the issue tracker of this repository to discuss potential improvements.


## Development: beyond adding content

To change the inner workings of the GitHub page, clone the project and build the page locally with [Jekyll](https://jekyllrb.com/).

**Important:** Make sure that your local build reflects the desired effects of your changes before pushing to the `main` branch.

**Prerequisites:** The following steps install the dependencies.

```
sudo apt-get install rubygems ruby-dev

cd /path/to/ml2r-center.github.io
sudo gem update bundler
bundle install
```

**Preview:** The page will be hosted at http://127.0.0.1:4000.

```
cd /path/to/ml2r-center.github.io
bundle exec jekyll serve
```

The website is based on Jekyll's [minima](https://github.com/jekyll/minima) theme. You can change the layout by copying the default file from this theme to this repository and make the desired changes.
