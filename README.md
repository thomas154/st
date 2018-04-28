# My st config

## Some patches added are:

+ copy to clipboard
+ solarized colors (light and dark toggleable)
+ vertcenter
+ scrollback with keyboard
+ scrollback with mouse without pressing any key
+ external pipe (awesome feature which I use to grab urls).

## Some Keyboard shortcut used are

+ Alt-Tab Toggle light/dark mode
+ Alt-k and Alt-j scroll back/foward in history one line at a time
+ Alt-u To trigger external pipe feature
+ Alt-Shift-pageUp to increase font size
+ Alt-Shift-pageDown to decrease font size
+ Alt-Shift-Home  back to default font size
+ Alt-Shift-c copy
+ Alt-Shift-v paste
 
## Installation

```
make
sudo make install
```

## Transparency

Transparency patch not added as I use compton for transparency.

## Patching
Patches can be applied by downloading diff file from suckless site.
```
patch < patchName.diff
make
sudo make install
```

And to remove patch

```
patch -R < patchName.diff
make
sudo make install
```
# Note:
To use url grabbing feature download the urlopener file 
 
replace
```
~/scripts/st-urlopener/./urlopener
``` 
at line 203 of config.h

with
```
static char *openurl[] = { "/bin/sh", "-c", "sed 's/ssh:\\/\\///g' | pathToTheUrlopenerFile./urlopener", "externalpipe",NULL, NULL  };
```


