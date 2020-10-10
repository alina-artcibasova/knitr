# knitr (for use with tikz and Windows)

UPD: it seems that as of at least [knitr 1.21.14](https://github.com/yihui/knitr/commit/5f5e2e643fcdda45f67ea785d0d9ff40c3568ee1) dependency on imagemagick has been removed.

This repo was created to tackle the issue (https://stackoverflow.com/questions/49368760/minimal-working-example-of-tikz-usage-in-bookdown?noredirect=1#comment95935428_49368760) which arises with knitr when
engine=tikz is used in one of the chunks. For it to work installation of
imagemagick (https://www.imagemagick.org/script/index.php) and GhostScript
(https://www.ghostscript.com/) is needed. As well as that, on line 281 of
R/engine.R the path to imagemagick's convert is hardcoded cause otherwise
it seems that Windows interprets it as 'convert.exe' from System32 directory (https://stackoverflow.com/questions/26961773/imagemagick-path-not-being-recognized-with-engine-tikz-in-knitr)

## Installation

devtools::install_github('darthaline/knitr')
