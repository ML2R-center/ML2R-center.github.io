# https://ml2r-center.github.io/

GitHub pages featuring ML2R-affiliated software repositories.

## Adding content

To add your software repositories, you simply need to add a list entry to the `index.md` Markdown file (you can even do so in GitHub's online editor without cloning the project locally). GitHub pages will re-build the website accordingly.

## Local preview

Having cloned the project, you can build the GitHub page locally with [Jekyll](https://jekyllrb.com/). 

**Prerequisites:** The following steps install all necessary dependencies.

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
