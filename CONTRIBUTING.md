## Getting started

Once the repository is cloned somewhere, `cd` into that directory and run the
following commands. You only need to do `install` once to get started, then use
`update` very occasionally (if we ever update gems).

```bash
# Tools that must be installed globally.
$ gem install bundler

# first time
$ bundle install

# occasional updates
$ bundle update
```

## Normal development

To run a server that auto-generates the new site when you save files, run the
following command at the root of your site (to start the Jekyll server).

```bash
$ jekyll serve
```

> To run Jekyll in a way that matches the GitHub Pages build server, run Jekyll with Bundler. Use the command `bundle exec jekyll serve`.

When everything is OK, your site should now be available at `http://localhost:4000`.
