# vidcat

Simple shell script for concatenating video files of the same dimensions
and encoding.

This simply copies the data and does not re-encode, so it's speedy
(hours of video will concatenate in seconds).

## Prereqs

* ffmpeg
  * Mac users can install with
    ```
    brew install ffmpeg
    ```

## Install

### Mac/Linux/Unix

1. Copy `vidcat` somewhere that you want it.
2. `cd` to that directory.
3. `chmod 755 vidcat`
4. When you want to run it, specify the path:
   ```
   ~/mydir/vidcat *.mp4 outfile.mp4
   ```

Alternately, you can add that directory to your `PATH` variable so that
the shell can always find `vidcat`. E.g.

```
mkdir -p ~/.local/bin
cp vidcat ~/.local/bin
chmod 755 ~/.local/bin/vidcat
```
and in your `~/.bashrc` file:

```
export PATH=$PATH:~/.local/bin
```

then relaunch your shell. You should be able to then:

```
vidcat *.mp4 outfile.mp4
```

from any directory.

### Windows

1. Install bash somehow
2. Install `vidcat` kinda like for Mac
3. ...
4. Profit!


## Usage

```
vidcat vidfile [ vidfile ... ] outfile
```

`vidcat` will steadfastly refuse to overwrite any existing file.
Manually remove your outfile ahead of time if you need to overwrite it.

### Examples

```
vidcat zoom*mp4 outfile.mp4

vidcat zoom_1.mp4 zoom_3.mp4 outfile.mp4

vidcat *.mp4 outfile.mp4
```

