# vidcat

Simple shell script for concatenating video files of the same dimensions
and encoding.

This simply copies the data and does not re-encode, so it's speedy
(hours of video will concatenate in seconds).

## Prereqs

* ffmpeg

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
