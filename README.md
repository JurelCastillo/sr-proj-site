# Development

- Requires `Ruby >= 2` 
- if you have never used ruby, you're going to need to install it from the website, then run 
- `gem install bundler`
- NOTE: Because we cannot run the 'gem' command, we cannot work on the website on the se machines
- Then you run this to build the website
- `$ bundle install`
- and This to actually serve the website locally.
- `$ bundle exec jekyll serve`
- It will run on localhost:4000

# Adapting the content

- Edit the contact info JSON files in `_data/` (done)
- Edit your project metadata in `_config.yml` (done)
- Add new pages as markdown files in `./`
- Add navigation links in `_includes/page-header.html`
- Most changes will be done in the new files, and the `_includes/page-header.html`. If something looks good in your local environment
- it might not look good once on the website, so tread lightly.

# Publishing

- Log into your VM and setup your ssh keys (done)
- Run `jekyll build` on your machine (this is the local machine you're running the other things on)
- Push your site to the vm:
  `scp -r _site/* <VM name>@nitron.se.rit.edu:~<VM name>/public_html`
- If you're using windows, you're going to need to install WinScp. Its fairly lightweight, and pretty simple.

# License

This work is licensed under a [Creative Commons Attribution 4.0 International](https://creativecommons.org/licenses/by/4.0/) license.

[1]: https://jekyllrb.com/
[2]: https://pages.github.com/
[3]: https://github.com/jasonlong/cayman-theme
