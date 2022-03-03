# Dustkid TV

Plays recent Dustforce replays from dustkid.com


## Dependencies

 [Python 3](https://www.python.org/downloads/) and the following libraries are needed to run this program:

```
pillow
numpy
pandas
```

Install them with `pip install pillow numpy pandas` or any other preferred method.

It also needs [dustmaker](https://github.com/msg555/dustmaker) version >= 1.1.1: download [this](https://github.com/msg555/dustmaker/archive/refs/heads/main.zip) and install with `python setup.py install`.


## Usage

This assumes that you are using [Dustmod](https://dustmod.com/).

First, set file associations in Dustmod (Dustmod → About → Set file associations).

Find your Dustforce game folder. If you are using the Steam version, it will look something like `C:/Program Files (x86)/Steam/steamapps/common/Dustforce/`. Edit the `config.json` file in this program's main folder so that it points to your Dustforce game folder and your Dustmod executable:

```
{
  "path":    "C:/Program Files (x86)/Steam/steamapps/common/Dustforce/"
  "dustmod": "C:/Program Files (x86)/Steam/steamapps/common/Dustforce/dustmod.exe",
}
```

Run `main.py` to launch Dustkid TV.


## Self-contained executable

Optionally, `build.py` uses `pyinstaller` to create a standalone executable, which can be used on systems where Python and the libraries listed above are not available.


## Notes

Dustkid Daily replays will be played incorrectly if you have not downloaded/played today's daily. Access Dustkid Daily in the Dustmod Community Nexus to fix them.

This program caches custom map files and replay files. It is safe to delete the contents of the `dfreplays` and `dflevels` folders.


## Thanks

Thanks to Msg and Joel for sharing ideas / dustbot code.  
Thanks to Jdude for patiently listening to a boring analysis of player trajectories.  
Thanks to Skyhawk for help with Tkinter.  
Wallpaper by @tashizuna
