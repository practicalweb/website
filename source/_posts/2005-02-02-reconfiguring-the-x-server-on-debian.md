---
layout: post
title: ! 'Reconfiguring the X server on Debian '
created: 1107360753
comments: true
categories:
- linux
- debian
---
This is one of those tasks that I do infrequently and forget how it works…
<div class="post-entry">
<p>
I just got a nice big new monitor <img class="wp-smiley" src="http://www.uncertainty.org.uk/wordpress/wp-includes/images/smilies/icon_smile.gif" alt=":-)" /> 
</p>
<p>
The command is
</p>
<pre>
dpkg-reconfigure xserver-xfree86
</pre>
<p>
But this will silently fail to update the XF86Config-4 file if the
file has been modified, if you read the file carefully you will see a
useful explanation - but I missed this.
</p>
<pre>
# XF86Config-4 (XFree86 X Window System server configuration file)
#
# This file was generated by dexconf, the Debian X Configuration tool, using
# values from the debconf database.
#
# Edit this file with caution, and see the XF86Config-4 manual page.
# (Type &quot;man XF86Config-4&quot; at the shell prompt.)
#
# This file is automatically updated on xserver-xfree86 package upgrades *only*
# if it has not been modified since the last upgrade of the xserver-xfree86
# package.
#
# <strong>If you have edited this file but would like it to be automatically updated
# again, run the following commands as root</strong>:
#
#   cp /etc/X11/XF86Config-4 /etc/X11/XF86Config-4.custom
#   md5sum /etc/X11/XF86Config-4 &gt;/var/lib/xfree86/XF86Config-4.md5sum
#   dpkg-reconfigure xserver-xfree86
</pre>
<p>
see also<br />
<a href="http://www.tulrich.com/geekstuff/debian_tricks.html">www.tulrich.com/geekstuff/debian_tricks.html</a><br />
<a href="http://bugs.debian.org/cgi-bin/bugreport.cgi?bug=223929">bugs.debian.org/cgi-bin/bugreport.cgi?bug=223929</a>
</p>
</div>
