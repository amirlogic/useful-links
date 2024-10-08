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

### Adding audio to video

```bash
ffmpeg -i video.mp4 -i audio.mp3 -map 0:v -map 1:a -c:v copy -c:a copy -shortest output.mp4
```
With the -map 0:v -map 1:a arguments, the video track from the first input (0:v) and the audio track from the second input (1:a) are mapped to the output.
The -c:v copy arguments tell FFmpeg not to re-encode the video.
By default, when FFmpeg receives multiple input files, it uses the length of the longest input file as the output duration. We're going to use the shortest duration here, so we'll use -shortest.

### Reverse video

```bash
ffmpeg -i originalVideo.mp4 -vf reverse reversedVideo.mp4
```

### Convert video

```bash
ffmpeg -i "input_file_name.mkv" -map 0 -c copy "output_file_name.mp4"
```
