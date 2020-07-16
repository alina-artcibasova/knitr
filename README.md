# knitr (for use with tikz and Windows)

This repo was created to tackle the issue (https://stackoverflow.com/questions/49368760/minimal-working-example-of-tikz-usage-in-bookdown?noredirect=1#comment95935428_49368760) which arises with knitr when
engine=tikz is used in one of the chunks. For it to work installation of
imagemagick (https://www.imagemagick.org/script/index.php) and GhostScript
(https://www.ghostscript.com/) is needed. As well as that, on line 281 of
R/engine.R the path to imagemagick's convert is hardcoded cause otherwise
it seems that Windows interprets it as 'convert.exe' from System32 directory (https://stackoverflow.com/questions/26961773/imagemagick-path-not-being-recognized-with-engine-tikz-in-knitr)

## Installation

devtools::install_github('darthaline/knitr')
