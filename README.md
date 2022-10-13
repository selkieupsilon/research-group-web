Website for Wing Ying Chow's Lab at University of Warwick, UK
=============================================================

[https://wychowlab.org/](https://wychowlab.org/)


Background
=======================

This is a [Jekyll][]-based Web site based on the work of the [sampa][] group at the University of Washington. It was forked from [this repository][uwsamparepo] and detached after significant modifications.

This work is licensed under a [Creative Commons Attribution-NonCommercial 4.0 International License][license].

[Jekyll]: http://jekyllrb.com/
[sampa]: http://sampa.cs.washington.edu/
[license]: https://creativecommons.org/licenses/by-nc/4.0/
[uwsamparepo]: https://github.com/uwsampa/research-group-web

Modifications from uwsampa template
--------
- adapted and optimized the build process for [GitHub Pages](https://pages.github.com/)
- improved `.gitignore` using [Toptal's gitignore tool](https://www.toptal.com/developers/gitignore/)
- added Gemfile for a consistent Jekyll build environment using [Bundler][]
- added [jekyll-seo-tag plugin][jekyll-seo-tag], mostly for improved [Twitter cards][twittercards]
- added jekyll-feed and jekyll-sitemap plugins
- updated from [Bootstrap][] 3 to 5
- updated from [Font Awesome][fa] 4 to 6, originally for the ORCID logo, but possibly now more for the [fun effects](https://fontawesome.com/docs/web/style/animate)
- updated from [jQuery][] 3.5.1 to 3.6.1
- added [favicon generated from fontawesome](https://gauger.io/fonticon/)
- used [pylatexenc][pylatexenc] to convert LaTeX-encoded parts of website back to text
- refactored parts of default.html/index.html as includes
- typography: test with [Fontjoy][], served with [Google web fonts][gwf]
- implemented some accessibility provisions such as `alt` tags for images and screen readers (`aria`)
- renamed master to main (see [github/renaming](https://github.com/github/renaming))
- removed "faculty" as being used for a single-PI lab website
- added [lightbox][]
- implemented a covers gallery on the publication page
- implemented checking for broken links using [html-proofer][] (gem)

[Bundler]: https://bundler.io/
[jekyll-seo-tag]: https://github.com/jekyll/jekyll-seo-tag
[twittercards]: https://developer.twitter.com/en/docs/twitter-for-websites/cards/overview/abouts-cards
[pylatexenc]: https://pylatexenc.readthedocs.io/en/latest/latex2text/
[fontjoy]: https://fontjoy.com/
[gwf]: https://fonts.google.com/
[jQuery]: https://jquery.com/
[lightbox]: https://lokeshdhakar.com/projects/lightbox2/
[html-proofer]: https://github.com/gjtorikian/html-proofer
[bibble]: https://github.com/sampsyo/bibble/
[Python]: https://www.python.org/
[fork]: https://github.com/wychowlab/research-group-web/fork


Building
--------

The requirements for building the site are:

* [Bundler][]: run `gem install bundler`
* [Jekyll][]: run `gem install jekyll`
* gems listed in the Gemfile - though you can comment out parts you don't need
* [bibble][]: available on `pip`
* ssh and rsync, only if you want to deploy directly.

`make` compiles the bibliography and the website content to the `docs`
directory. To preview the site, run ``make serve`` and head to
http://localhost:4000.


Deploying to GitHub Pages
-----------------------

This template is optimized for hosting the site on GitHub Pages using a custom domain in `CNAME`. You can pick which branch you deploy the site on. A new commit/push to GitHub will trigger a rebuild.


