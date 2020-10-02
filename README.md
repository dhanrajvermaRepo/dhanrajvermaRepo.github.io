# Awesome-CV Second Assignment
[View Site](https://moya10.github.io/awesome-cv/)

## Installation & setup guide
This template is designed to be hosted using GitHub pages and so that's what these instructions will cover. If you plan on hosting it seperately then there might be some extra steps that we wont cover.

Before starting it might be useful to familiarise yourself with [Jekyll](https://jekyllrb.com/docs/home/), [Markdown](https://www.markdownguide.org/getting-started) and [GitHub pages](https://pages.github.com/).


## Running locally

Before you start make sure you have *Ruby* and the gems for *Jekyll* installed locally. You can find out how to do that [here](https://jekyllrb.com/docs/installation/).

1. Clone your resume repository locally *(if you haven't already)*
2. `cd [your-repository-name]`
3. `bundle install`
4. `bundle exec jekyll serve`
5. Open your browser to `http://localhost:4000`

Any changes you make will automatically build and you will be able to see these by refreshing your browser.

*Note: You will need to re-run `bundle exec jekyll serve` to see changes made in `_config.yml`.*

## LaTex - CV

### Locally

Before you start make sure you have *pandoc* [here](https://pandoc.org/installing.html) and *MikTeX* [here](https://miktex.org/download) installed in your computer.

Then put inside makefile the code below:

`TEX = pandoc details.yml `

`src = template.tex`

`FLAGS =`

`resume.tex : $(src)`

`	$(TEX) $(filter-out $<,$^ ) -o $@ --template=$< $(FLAGS)`

` .PHONY: clean`

`clean :`

`rm resume.tex`
  
This will create the *resume.tex* file. Run it locally to produce the *resume.pdf*.

In *_config.yml* add the cv option and a link to download the *resume.pdf* file.

## Upload

Upload the whole .git project in your repository and create the *gh-pages* branch.


## Continuous Integration

To set up Travis CI, create .travis.yml file in your repository:

See Trvais CI build output 

link to [build](https://travis-ci.com/moya10/awesome-cv)


