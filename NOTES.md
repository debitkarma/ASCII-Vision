# How I Got This Working

`uv venv` to make virtualenv
`uv python pin 3.8` to pin python version
`uv pip install imageio imageio-ffmpeg numpy keyboard numexpr`
get older version of pillow that uses `getsize` method (deprecated in 10)
get python dev stuff so older pillow version can be built using python.h
`apt install python3-dev`
`uv pip install pillow==9.5.0`
`apt install python3-tk`

edit app.py

find `zoomed` and change it to `normal`

change vars in `app.py`
```
BACKGROUND_COLOR = "black"
FONT_COLOR = "white"
FONTSIZE = 1
BOLDNESS = 2

ASCII = 1
FILTER = 1
BLOCKS = 1

```

to run:

```sudo su
source .venv/bin/activate
python app.py```
