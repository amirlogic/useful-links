# FFMpeg

Command line tool to converts and edits videos


## Extract audio from video

To find out which codec your audio track is using:

```ffmpeg -i inputVideo.mp4 -hide_banner```

If both the input and outputs are in aac format:

```ffmpeg -i inputVideo.mp4 -acodec copy outputAudio.aac```

Extract audio to MP3:

```ffmpeg -i inputVideo.mp4 outAudio.mp3```

Extract audio to WAV:

```ffmpeg -i inputVideo.mp4 outAudio.wav```

Extract part of video:

```ffmpeg -ss 00:03:30 -to 00:03:48 -i input.mp4 -c copy output.mp4```
