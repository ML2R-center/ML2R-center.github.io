# [ml2r-center.github.io](https://ml2r-center.github.io/)

GitHub pages featuring ML2R-affiliated software repositories.

## Adding content

Adding an entry to `_data/software.yml` will publish your software on the GitHub page. You can [edit this file online](https://github.com/ML2R-center/ML2R-center.github.io/edit/main/_data/software.yml).

```yaml
- name: title of the supplemented paper OR name of the library
  type: "e" OR "l"
  url: where to link (ONLY PUBLIC REPOSITORIES)
  description: paper authors and venue OR sentence about the library
  areas: [ "h", "r", "t", "q", "o" ]
  biblink: url to obtain bibtex of corresponding publication, e.g. dblp (see below)
  keywords: [ "optional", "keywords", "that are not redundant(!) with the description" ]
```

- The `type` and `areas` shortcuts will display colored badges.
- All of the content (name, type, areas, description, keywords) can be used to search for entries.
- Only use keywords that do not appear in the rest of your entry.
- When a change is pushed to the `main` branch, GitHub pages will re-build the website immediately.

shortcut | field | meaning
-------- | ----- | -------
e        | type  | experiment
l        | type  | library
h        | areas | hybrid
r        | areas | resource-aware
t        | areas | trustworthy
q        | areas | quantum
o        | areas | other

**Bibtex Link:**
Providing a bibtex link is optional. If you don't want to have it, please remove the biblink field from your entry.

If you like / it is applicable, you can provide a link to a reference to a corresponding article in bibtex format. 
If your paper is already published and indexed by dblp, you can navigate to your publication, e.g.

https://dblp.uni-trier.de/rec/journals/ki/Wrobel97.html

and select bibtex format by clicking on the little download button, or by appending ``?view=bibtex`` to the url:

https://dblp.uni-trier.de/rec/journals/ki/Wrobel97.html?view=bibtex

Otherwise, any other (persistent!) url will do. Google scholar, e.g. also provides references in bibtex format. 


## Need help?

Instead of pushing to the `main` branch directly, feel free to open a pull request and let someone check your entries.


## Feature requests

Please use the issue tracker of this repository to discuss potential improvements.


## Development (not needed to add content)

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
