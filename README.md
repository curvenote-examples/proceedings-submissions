# Template for Conference Proceedings

> [!NOTE]
> This is a template repository designed for editorial teams at journals, lab group websites,
> or personal sites who are managing a focused collection of articles, such as
> conference proceedings, consortium articles, or lab-group papers.
> The editorial process setup by this repository involves a single,
> centralized GitHub repository where all operations — submission, review, revision, and acceptance — are managed.
>
> This approach leverages the collaborative aspects of GitHub for peer-review and can offer full
> transparency of the editorial decisions, and represents a relatively simple editorial workflow.

Welcome to our conference `[our conference name and date, etc.]`, this year we are accepting submission using Curvenote and a centralized submission process that is facilitated by GitHub pull requests.

## Author Instructions

We accept three types of papers that are powered by the `mystmd` build engine ([mystmd.org][myst]): MyST Markdown articles, LaTeX documents, or Jupyter Notebooks. All submissions formats are powered by [`mystmd`][myst], and are focused on the web-first presentation of scientific content. Please only use LaTeX if you are already familiar with writing papers in LaTeX, and note that many macros will not be supported.

There are templates in the `articles` folder that can be used as a starting point for your submission. These templates include formatting, references, math, tables and images. This overview assumes familiarity with GitHub and Git.

<!-- Expand sections of this guide for targeting authors with less familiarity with Git or GitHub -->

- Fork and clone this repository
- In your local copy of the repository, create a branch named `article/<last_name>`, where `<last_name>` is your last name or appropriate identifier for your submission.
- Copy one of the template folders in `articles` to a new folder with your name
- Update the ID in the `myst.yml` and title, author, and affiliation information following the instructions in the configuration
- Install [curvenote][curvenote-install] and [nodejs](https://nodejs.org)
- Run `curvenote start`, open the main article file, edit the content, save and see the changes in real time
- Write up your research, including any associated Jupyter Notebooks, reproducible content etc.
- Commit your content to git, ensuring you only make changes in your single folder
- Open a pull request against the origin repository
- See the GitHub actions run, and make a comment on your PR with the check results and a link to your preview
<!-- update `venue` here as well as add `--kind` and/or `--collection` if appropriate -->
- To run these checks locally, you may run `curvenote check <venue>`
- An editor will assign reviewers, who will make comments in GitHub, and you can respond to the comments until the reviewers and editors are satisfied with your submission. On each commit, a new preview will be made.
- The editor will mark the pull-request as accepted and merge it
- There may be extra steps the editorial team takes to make your submission live

## Templates

There are example templates provided that provide a starting place for your proceedings, the linked PRs have comments to the build process as examples.

- MyST Markdown with supporting Jupyter Notebooks [article.md](./articles/00_template_full/article.md) (PR: [#1](https://github.com/curvenote-examples/proceedings-submissions/pull/1))
- Jupyter Notebook as an article [article.ipynb](./articles/00_template_nb/article.ipynb) (PR: [#2](https://github.com/curvenote-examples/proceedings-submissions/pull/2))

[myst]: https://mystmd.org
[install]: https://mystmd.org/guide/quickstart
[curvenote-install]: https://curvenote.com/docs
