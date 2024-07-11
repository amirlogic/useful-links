# FFMpeg

Command line tool to converts and edits videos


```-i``` input

```-c``` encoding  ```-c copy``` not re-encoded

```-ss``` start position

```-to``` end position


## Extract audio from video

To find out which codec your audio track is using:

```ffmpeg -i inputVideo.mp4 -hide_banner```

If both the input and outputs are in aac format:

```ffmpeg -i inputVideo.mp4 -acodec copy outputAudio.aac```

Extract audio to MP3:

```ffmpeg -i inputVideo.mp4 outAudio.mp3```

Extract audio to WAV:

```ffmpeg -i inputVideo.mp4 outAudio.wav```


## Extract part of video:

```ffmpeg -ss 00:03:30 -to 00:03:48 -i input.mp4 -c copy output.mp4```


## Concat two or more videos

Create a text file and 

join.txt

```
file filename1.mp4
file filename2.mp4
```

Then run this in bash:
 
```bash
ffmpeg -f concat -safe 0 -i join.txt -c copy output.mp4
```

### Remove audio

```bash
ffmpeg -i input.mp4 -an -c:v copy output.mp4
```


### Convert video

```bash

```