vwallpaper
==========

Simple set of shell scripts which sets an video as wallpaper.

All you need is xwinwrap, in doubt use the bundled one, and mplayer or mplayer2.
I recommend mplayer2, the "fixed" version of mplayer.

Usage
-----

To set a video wallpaper:

    vwallpaper <path_to_video_file>

vwallpaper creates a named pipe in your home directory and starts mplayer2
in slave mode. To control mplayer2 just use ```echo```. E.g. ```echo "command" >> ~/.vwallpaper.pipe```.

If you want to pause or resume the playback:

    $ echo "pause" >> ~/.vwallpaper.pipe

And to stop the playback:

    $ echo "quit" >> ~/.vwallpaper.pipe

See ```mplayer2 -input cmdlist``` for details.

If you want to watch a movie on your desktop, use ```vwallpayer```.
Here you can control mplayer2 as usual. ```vwallpaper``` does not
create any pipes.

    $ vwallpaper <cool movie I want to watch.mkv>

### configuration

To do any configuration, you'll need to hack the scripts.

xwinwrap
--------

While ```mplayer --rootwin``` doesn't work well with any[1] composite manager, xwinwrap is needed.
The initial maintainer of xwinwrap stopped maintaining it, so I decided to bundle it.
You will find the orgininal copy of the bundles version here[2]: 
 
 * <https://launchpad.net/xwinwrap>
 * or checkout the home page <http://tech.shantanugoel.com/projects/linux/shantz-xwinwrap>

mplayer / mplayer2
------------------

Here you'll get mplayer and/or mplayer2:

 * <http://www.mplayerhq.hu/>
 * <http://www.mplayer2.org/>

* * * * * * * * *

[1] As far as I can tell

[2] It's **not the original** version of xwinwrap! It's a modified one.
