# [RappleShots by Ray](https://github.com/rayantony/RappleShots/)
========================

### [RappleShots](https://github.com/rayantony/RappleShots/) are Ray's Apple IOS-ish Screenshots in Linux with Image Magick

![Sample RappleShot&trade;](https://d39dlwgeopmdw0.cloudfront.net/assets/test/rappleshots/thrones_rappleshot.png)

My personal system of making *screenshots that don't suck* is designed for use with nautilus to give context menu click method of highlight and swift creation as in (1 click) processing, on multiple image files of various extensions into cool Apple IOS Style Screen shots. 

[PREVIEW LINK](http://statspring.com/?https://raw.githubusercontent.com/rayantony/RappleShots/master/demo.html)

If using gnome-screenshot the options are simple on the cli for example 
```bash
gnome-screenshot -b -w -d 2 --border-effect=shadow
```
should give you the active or current window with a drop shadow. 
```bash
gnome-screenshot -b --border-effect=shadow -i 
```
will do the same but operate with the gui control box for configs. And of course there are innumerable methods of setting defaults in your alias file in compiz 'ccsm' editor, gconf, the .desktop file etc.

If though you want to have a separate processing solution to cover use cases where for instance the file is already made and not with the aforementioned options configured the simplest way is ImageMagick library. Here's the basic command 
```bash
convert [screenshotimagefile] \( +clone -background black -shadow 80x20+0+15 \) +swap -background transparent -layers merge +repage [screenshotimagefile_rappleshot_style]
```

Same as in my other forthcoming repo of ImageMagick automation. I f'n love imagemagick, prcessing on the command line or 1 click shell "apps"? Seriously cool. I can handle 200 files before gimp even opens, and as usual do it on a chromebook with 12.04 ray-buntu (like chrubuntu) 

If you use Nautilus/Unity/Gnome then drop rappleshots.sh in $HOME/.gnome2/nautilus scripts/... 
```bash
git clone https://github.com/rayantony/RappleShots.git && \
cd RappleShots && \
sudo cp rappleshots.sh $HOME/.gnome2/nautilus-scripts/rappleshot && \
sudo chmod ug+rwx $HOME/.gnome2/nautilus-scripts/rappleshot && \
sudo chown $USER:$USER $HOME/.gnome2/nautilus-scripts/rappleshot &&
```
Depending on your packages which is outside the scope of this simple app, you should be good to go context menu right click action, and ready to deal in bulk!

Typical run would be like this from the terminal:
```bash
. rappleshots.sh file
```
The above example will create a copy of that file in the working directory appended with "_rappleshot" in the basename. You can run multiples from the cli like so:
```bash
. rappleshots.sh file1 file2 file3
```
or
```bash
for pic in [your list or set];do . rappleshots.sh "$pic";done
```

Or however you wish. Run it from github "curl" the [raw file](https://raw.githubusercontent.com/rayantony/RappleShots/master/rappleshots.sh) if it pleases, whatever. btw thats probably something like this: *export rappleit=`curl -L https://raw.githubusercontent.com/rayantony/RappleShots/master/rappleitrawfunc|tail --lines 8`
ok, that needs some work to escape and add right or not worth the risk, moving on...

The nice part really is to have the basic rappleshot line reachable when you need it as few would remember it syntactically unless they are imagemagick uber nerds. As well, to be able to have a way to abstract this handy item to take in x files process and rename appropriately the copies, which is the real value with this, the template.


Have Fun!
- by ray anthony 
@rayantony

[![Bitdeli Badge](https://d2weczhvl823v0.cloudfront.net/rayantony/RappleShots/trend.png)](https://bitdeli.com/free "Bitdeli Badge")

 [twitter.com](http://platform.twitter.com/widgets/follow_button.html?screen_name=rayanthonyrcc)
 
 copyright 2015 [ray anthony](http://rayanthony.io)&copy; all applicable rights reserved all liabilities waived
 
 [oneworldlicense.com](http://oneworldlicense.com) means open source, free, and made with ♡ in f'n nano and hosted at Github



