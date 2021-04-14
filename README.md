# [ml2r-center.github.io](https://ml2r-center.github.io/)

GitHub pages featuring ML2R-affiliated software repositories.

## Adding content

Adding an entry to [`_data/software.yml`](https://github.com/ML2R-center/ML2R-center.github.io/blob/main/_data/software.yml) will publish your software on the GitHub page.

```yaml
- name: title of the supplemented paper OR name of the library
  type: "e" OR "l"
  url: where to link (ONLY PUBLIC REPOSITORIES)
  description: paper authors and venue OR sentence about the library
  areas: [ "h", "r", "t", "q", "o" ]
  biblink: url to obtain bibtex of corresponding publication, e.g. dblp (see below)
```

Here, the `type` shortcuts stand for "experiment" and "library" and will be displayed as badges next to the title. The `area` shortcuts "hybrid", "resource-aware", "trustworthy", "quantum", and "other" will be displayed similarly. All badges can be used as a filter criterion in the search bar.

When a change is pushed, GitHub pages will re-build the website immediately.

### Bibtex Link
Providing a bibtex link is optional. If you don't want to have it, please remove the biblink field from your entry.

If you like / it is applicable, you can provide a link to a reference to a corresponding article in bibtex format. 
If your paper is already published and indexed by dblp, you can navigate to your publication, e.g.

https://dblp.uni-trier.de/rec/journals/ki/Wrobel97.html

and select bibtex format by clicking on the little download button, or by appending ``?view=bibtex`` to the url:

https://dblp.uni-trier.de/rec/journals/ki/Wrobel97.html?view=bibtex

Otherwise, any other (persistent!) url will do. Google scholar, e.g. also provides references in bibtex format. 

## Local preview and web development

Having cloned the project, you can build the GitHub page locally with [Jekyll](https://jekyllrb.com/). 

**Prerequisites:** The following steps install the necessary dependencies.

```
sudo apt-get install rubygems

cd /path/to/ml2r-center.github.io
gem update bundler
bundle install
```

**Preview:** The page will be hosted at http://127.0.0.1:4000.

```
cd /path/to/ml2r-center.github.io
bundle exec jekyll serve
```

The website is based on Jekyll's [minima](https://github.com/jekyll/minima) theme. You can change the layout by copying the default file from this theme to this repository and make the desired changes.
