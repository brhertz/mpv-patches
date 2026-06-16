__mpv-patches__

Assortment of mpv patches.<p>&nbsp;</p>

<ins>1. 0001-osd-list-reverse-b9e6030.patch</ins>

Patch that reverses commit b9e6030, to give us back a bullet-list like osd list layout (playlist, chapter list, ...). Note that we don't undo everything in that commit, all that interests us is to restore the bare, relevant functionality. Also because the less we change, the higher the chance the patch applies cleanly in the future.

Tested with master on commit 304426c, last release before was 0.41.0.

_Before:_<br><br>
![before patch](/images/0001-osd-list-b9e6030.jpg)

_After:_<br><br>
![after patch](/images/0002-osd-list-b9e6030-reverted.jpg)
<p>&nbsp;</p>

<ins>2. 0002-osd-list-hide-white-circles.patch</ins>

Additionally to 0001, hide the 'white circles' using libass.

Wondering what they're there for anyway? It's because when you're using a variable width font you won't find a 'blank' of the same width, resulting in misalignment. If you use a monospace font though you can simply replace the white circle #define in the source code with a unicode em space to get the same effect.

Tested with same mpv version as 0001.

_After:_<br><br>
![after patch](/images/0003-osd-list-white-circles-hidden.jpg)
