# hexo-spanner

## DORMANT PROJECT: Preserved for Archival Purposes ##

The authoring folder for the Spanner Wingnut blog

This project provides source-code management and preservation of the desktop development folder for the [Spanner Wingnut Muddleware Labs](http://orcmid.com/BlunderDome/wingnut) blog.

Although the project provides code in the open, it is focused entirely on the authoring process for a specific blog.  

## Original Sources ##

The authoring of the Wingnut blog is performed on a Windows 10 desktop using node.js with the [hexo](https://hexo.io/) blog-generation framework.  The default hexo install is into a folder named `spanner`.  `Spanner` includes generator-installed artifacts as well as subfolders where source pages of the blog are authored.  The `hexo-spanner` git preserves only those parts necessary for reconstruction/reconstitution of the authoring folder if the need arises.

`hexo-spanner` is not a fork of the hexo GitHub.  `hexo-spanner` mirrors the `spanner` folder after its initialization using hexo.  If there are fixes/improvements that may be valuable for hexo itself, they will be transposed into a separate fork of the hexo project just for that purpose.

Default initialization of `spanner` will also introduce a default theme, `landscape`.  Multiple themes are available.  Inital setup with `landscape` is a getting-started convenience.  For Spanner Wingnut, it is the `landscape` theme that is being customized.

Because themes are developed and installed separately, the theme code for wingnut source-managed separate from `hexo-spanner`.  See the [hexo-theme-landscape-wingnut](https://github.com/orcmid/hexo-theme-landscape-wingnut) project for the customization of theme `landscape` as installed in the `spanner` folder.

## Related Material ##

This is a solo project.  A key goal is to achieve a customization for wingnut that can then be transposed into development folders for other blogs that I want to restore from their current dormant state.  

As an aid to myself, and anyone else who wants to see customization of a hexo-generated blog, there is narration in the managed-source materials and discussion on two blogs.

 * [Spanner Wingnut Muddleware Labs](http://orcmid.com/BlunderDome/wingnut) is operating well enough to account for further customization and test posts used in confirmation.
 * [Orcmid's Live Hideout](https://orcmid.wordpress.com/) carries additional information on how setup and customization of the hexo-based authoring progressed.  The tag [hexo](https://orcmid.wordpress.com/tag/hexo/} provides a list of posts specifically about hexo and its usage in the restoration of the Spanner Wingnut blog.
