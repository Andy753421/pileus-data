vpaste is a pastebin that uses Vim for syntax highlighting.

The pastebin
------------
* <http://vpaste.net/>

Source Code
-----------
Source code is available in git and [gitweb](/git/?p=vpaste)

    git clone git://pileus.org/vpaste

Embedding examples
------------------
vpaste allows pastes to be embedded in external websites:

<script type="text/javascript" src="http://vpaste.net/embed.js?ft=sh">
	#!/bin/bash

	echo Hello, World > test.txt
</script>

This can be done by including code in the script tag itself, as in the above
example, or by linking to an existing paste:

<script type="text/javascript" src="http://vpaste.net/embed.js?vpaste"></script>

A third way to use the embedding script is to include it once, possibly in the
in the header, and then call the `format_code('pre','vpaste')` function later
on to perform syntax highlighting on all the `<pre class="vpaste">` tags.

In this case, slightly more care must be taken to properly escape HTML
characters scuh as `<` and `>`.

<pre class="vpaste" title="ft=c">
	#include &lt;stdio.h&gt;

	int main(int argc, char **argv)
	{
		printf("hello, world");
		return 0;
	}
</pre>

<script type="text/javascript">format_code('pre', 'vpaste');</script>
