Nicola-RTL is a bunch of themes (and auxilliary files) for the [Nikola](http://nikola.ralsina.com.ar/) static site geneator that are:

1. Right to left.
1. Support dropdown menus.
1. Fixes problems with caption alignment, etc. (but you *have* to enter `:width:` at `.. figure::` and `.. image::` directives. Sorry about that).

### Demo

[This Hebrew site](http://MajorityOfOne.co.il) uses the `readable-rtl` theme.

### Limitations

So far I haven't thoroughly checked blog posts and galleries
([the site I needed this for](http://majorityofone.co.il) only needed "stories").

This would hopefully change eventually. Meanwhile, comments and pull requests are welcome, of course :)

### Installtion

* Install [Nikola](http://nikola.ralsina.com.ar/)
* Do `nikola init some-site-root-folder`
* Copy the `themes/` folder to _some-site-root-folder_
* cd into `some-site-root-folder` and edit `config.py`. and change `THEME` from `site` to `readable-rtl` or `spacelab-rtl`
* do `nikola build` and browse to see your result with `nikola serve`

### Adding dropdown menus

The (somewhat awkward) syntax is like this:


    'sidebar_links': {
        DEFAULT_LANG: (
            #...
            (
                (
                    ('/stories/about-nikola.html', 'About Nikola'),
                    ('/stories/handbook.html', 'The Nikola Handbook'),
                ),
                'Nikola docs'
            ),
            #...
            ),
        }
    }

### Converting new bootswatches

See the README files at `themes/*-rtl`. In one word: [R2](https://github.com/ded/R2#readme).
