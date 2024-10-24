# How I Got This Working

The original library is great, but dated. This the process I had to follow to get things installed and also working correctly. Minimal changes here, though I guess I could try to update stuff...

## Installation

  * `uv venv` to make virtualenv
  * `uv python pin 3.8` to pin python version
  * `uv pip install imageio imageio-ffmpeg numpy keyboard numexpr`
  * get older version of pillow that uses `getsize` method (deprecated in 10)
    get python dev stuff so older pillow version can be built using python.h
    `apt install python3-dev`
  * `uv pip install pillow==9.5.0`
  * `apt install python3-tk`

## Config

  * edit app.py
  * find `zoomed` and change it to `normal`

  * change vars in `app.py`
  * ```
    BACKGROUND_COLOR = "black"
    FONT_COLOR = "white"
    FONTSIZE = 1
    BOLDNESS = 2
    
    ASCII = 1
    FILTER = 1
    BLOCKS = 1
    ```

## Running

to run:

change to project dir

```sudo su
source .venv/bin/activate
python app.py```

## Sources

  * [Deprecation of `getsize` in pillow >= 10](https://github.com/tensorflow/models/issues/11040)
  * [Missing python.h](https://stackoverflow.com/questions/21530577/fatal-error-python-h-no-such-file-or-directory)

