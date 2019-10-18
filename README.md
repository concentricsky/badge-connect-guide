# Badge Connect Guide: The Unofficial Implmenter's Handbook to Open Badges 2.1

Editor: Nate Otto (Concentric Sky / Badgr - USA)
Contributors:

* This could be you (Your Company, Country Code)

This guide is intended to ease the implementation path for organizations wishing
to take advantage of the forthcoming Badge Connect API, which will be published
as Open Badges 2.1 by IMS Global Learning Consortium in 2020. A pre-release
version of the specification is available in [GitHub](https://github.com/IMSGlobal/openbadges-specification/tree/develop/ob_v2p1).

Contribute to this project on GitHub here. The Badge Connect Guide is published  
under an Apache 2.0 License.

It is published as a static HTML site built with [Hugo](http://gohugo.io/). It
uses a theme, **DocuAPI**, a beautiful multilingual API documentation theme for
Hugo. This theme is built on top of the beautiful work of [Robert Lord](https://github.com/lord)
and others on the [Slate](https://github.com/slatedocs/slate) project
([Apache 2 License](https://github.com/slatedocs/slate/blob/master/LICENSE)).
DocuAPI is also published under the same Apache 2.0 License.

## Use for Contributors

**Note:** this theme requires Hugo >= 0.56.0 to run. If you want to edit the SCSS styles, you need:

* The extended Hugo version.
* PostCSS CLI: npm install -g postcss-cli (TODO(bep) add a package.json)

See the [exampleSite](https://github.com/bep/docuapi/tree/master/exampleSite) and more specific its site [configuration](https://github.com/bep/docuapi/blob/master/exampleSite/config.toml) for the available options.

**Most notable:** This theme will use all the (non drafts) pages in the site and build a single-page API documentation. Using `weight` in the page front matter is the easiest way to control page order.
