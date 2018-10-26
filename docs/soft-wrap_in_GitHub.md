How to soft-wrap Rmarkdown in GitHub
===============================================

Up until just recently, Rmarkdown files on GitHub were rendered as HTML output. This is how plain Markdown files are rendered, like the README files in repositories, or the MD file that you're reading now. Around, 10 OCT 2018, @yihui (statistician and author of numerous very influential R packages and books) [requested that Rmd files no longer be rendered as markdown](https://yihui.name/en/2018/10/rmd-github/) on GitHub. There are several benefits of not rendering Rmd files as HTML output, which @yihui discusses in detail.

With the plain-text rendering of Rmd, **one annoyance is that a single line of text is not soft-wraped** -- i.e., if you have a long line, you have to scroll horizontally in your browser to see everything, and this makes reading Rmd files difficult. To avoid this, @yihui explains how to use the Google Chrome extension [Stylebot](https://chrome.google.com/webstore/detail/stylebot/oiaejidbmkiecgbjeifoejpgmdaleoha) to get Rmd lines to soft-wrap in GitHub ([it has been requested](https://github.com/github/markup/pull/1235) that GitHub soft-wrap Rmd automatically). 

**Here is the solution for Firefox users**, in case GitHub does not add the feature automatically: 

1. Download [Stylish](https://addons.mozilla.org/en-GB/firefox/addon/stylish/) as an add-on.  A small icon in the upper-right corner of your browser with an 'S' in the centre should appear.
2. Navigate to [GitHub](https://github.com).
3. Click on the 'S' icon
4. Click on the vertical elipses in the upper right of the pop-up. 
5. Choose the option 'Create new style'
6. Enter a name in the left of the window that pops up (e.g., 'Softwrap').
7. Add the code below to the centre

```
.type-rmarkdown .blob-code-inner {
  white-space: pre-wrap;
}
```

When you navigate to Rmd files such as [this one](https://github.com/StirlingCodingClub/version_control/blob/master/vc_notes.Rmd), all of the code should now be soft-wrapped. You can turn this on an off easily by clicking the 'S' and toggling from 'Stylish on' to 'Stylish off'.
