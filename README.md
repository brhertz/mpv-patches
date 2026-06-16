#### mpv-patches

Assortment of mpv patches.

<br/>

##### 0001-osd-list-reverse-b9e6030.patch

Patch that reverses commit b9e6030, to give us back a bulleted-list like osd layout (playlist, chapter list, ...). Note that we don't roll back everything in that commit, all that interests us is to restore the bare, relevant functionality. Also because the less we change, the higher the chance the patch applies cleanly in the future.

Tested on top of commit 304426c (last release before that commit was 0.41.0).

<details>
<summary>Before/after patch screencaps (click arrow to open):</summary>
<br/>
  
_Before:_

![before patch](/images/0001-osd-list-b9e6030.jpg)

_After:_

![after patch](/images/0002-osd-list-b9e6030-reverted.jpg)
</details>

<br/>

##### 0002-osd-list-hide-white-circles.patch

Additionally to 0001, hide the 'white circles' using libass.

Wondering what they're there for anyway? It's because when you're using a variable width font you won't find a 'blank' of the same width, resulting in misalignment. If you use a monospace font though you can simply replace the white circle #define in the source code with a unicode em space to get the same effect.

Tested on top of the same commit as above, i.e. 304426c, but with 0001 applied first.

<details>
<summary>After patch screencap (click arrow to open):</summary>
 <br/>

_After:_

![after patch](/images/0003-osd-list-white-circles-hidden.jpg)
</details>

<br/>

