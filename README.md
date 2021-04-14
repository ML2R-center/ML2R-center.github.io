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
```

**Explanation:** Here, the `type` shortcuts stand for "experiment" and "library" and will be displayed as badges next to the title. The `area` shortcuts "hybrid", "resource-aware", "trustworthy", "quantum", and "other" will be displayed similarly. All badges can be used as a filter criterion in the search bar. When a change is pushed to the `main` branch, GitHub pages will re-build the website immediately.

**Need help?** Instead of pushing to the `main` branch directly, feel free to open a pull request and let someone check your entries.

## Feature requests

Please use the issue tracker of this repository to discuss potential improvements.

## Development

Having cloned the project, you can build the GitHub page locally with [Jekyll](https://jekyllrb.com/). 

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

The website is based on Jekyll's [minima](https://github.com/jekyll/minima) theme. You can change the layout by copying the default file from this theme to the repository and make the desired changes.
