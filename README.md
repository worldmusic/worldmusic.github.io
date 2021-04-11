# World Music Textbook

This page houses the code for the [World Music Textbook](worldmusictextbook.org). It also contains some basic information about the tooling and technical processes used in maintaining the site.

<a rel="license" href="http://creativecommons.org/licenses/by-nc-nd/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-nd/4.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-nc-nd/4.0/">Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 International License</a>.

Feel free to email the editors at [editors@worldmusictextbook.org](mailto:editors@worldmusictextbook.org) if you are interested in contributing.

## Creating a collaborative textbook

Information about this project is available on the website itself. In an effort to enable similar projects or contributions to the technical elements of this one, the site's code is fully open and available within this repository.

### Version control and hosting

In an effort to lower costs, this site is built using Jekyll, a static site generator from GitHub. It was originally hosted using GitHub pages, a free service that is well integrated into GitHub's version control system. We moved to Netlify, however, to take advantage of the ability to deploy preview versions of the site when initiating a pull request through a new branch. For the purposes of a project like this, preview deploys are helpful for reviewing changes, including giving contributors the opportunity to proof pages before they are incorporated into the master branch.

The site was built using a standard Jekyll template, but the system allows for substantial flexibility. See the `_includes` and `_layouts` folders for examples of how smaller components (from headers to individual items within a listing) can be incorporated into a site. These are written in the `liquid` template language. The Jekyll documentation has more information.

## Print versions and redirects

We are hosting PDF files of our contributions through an external site for the sake of DOI preservation, but many of the contributions take advantage of the features of an online reading modality. To assist with this, we use static QR codes as images within the print versions of each article. These link to redirect pages within the `pdfs/` folder. The benefit here is that we can update any broken URLs both within the web version of the page (found in the `chapters` folder) and the PDF file. Hard-coding the destination URLs within the PDF's QR codes would prevent us from being able to make any updates.

The PDFs themselves are generated using LaTeX, a typesetting language that can be installed locally. Using `pandoc` (a command-line document conversion program) in conjunction with both LaTeX and Jekyll allows us to work from the same source files that are written in `markdown`. For more on how we create PDF files from the `markdown` files in the `chapter/` folder, see the README in the `pdfs/` folder.

## Issue and process tracking

Since our contributions move through a blind peer-review process, we organize the status of submissions outside of this repository. (We use shared Google Sheets and Google Docs files and a dedicated Slack channel for these purposes.) For other issues and update goals, we make use of GitHub's integrated issue tracker. Open issues are labeled as a "priority" for the next launch, a future "enhancement," or in similar ways. If you are interested in contributing to the technical development of this project, the issue tracker is a good place to look for ideas.

We use branches to share previews and proofs of accepted articles. Because these are a part of the public repository, they are open, though they should be considered as unpublished. When the authors and editors have finalized any changes, the preview branches are pulled into the master branch for publication. Netlify's preview deployments enable contributors to see actual previews instead of limiting them to code and markdown representations of their work.

## Resource listing

Resources are all listed within an `yaml` file in the `_resources` folder. Jekyll pull the individual items from this file and processes them according to the code in `_includes/resource.html`. Any suggested additions or edits to the resource list should be made to `_resources/resources.markdown`.