# ffmpeg Commands

## Convert flv/f4v to mp4
```
ffmpeg -i input.flv -codec copy output.mp4
```

## Extract Video
```
ffmpeg -i input.mp4 -c:v copy -an output-video.mp4
```

## Extraact Audio
```
ffmpeg -i t.mp4 -c:a copy -vn t-audio.aac
```
Note: the exported audio type must be the same as the audio type in the input file. If not, need more search about how to add transfer map. 

## Merge Video and Audio
```
ffmpeg -i t-video.mp4 -i t-audio.mp3 -c:v copy -c:a aac t.mp4
```

## Concat files
1. create mylist.txt file
```
file '1.mp4'
file '2.mp4'
file '3.mp4'
file '4.mp4'
file '5.mp4'
file '6.mp4'
```
2. run ffmpeg in CMD
```
ffmpeg -f concat -i mylist.txt -c copy output.mp4
```