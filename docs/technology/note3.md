# ffmpeg

- 合并视频和音频
```sh
ffmpeg -i ABC.mp4 -i ABC.m4a -c:a copy -c:v copy ABC.mp4
```

- 图片转视频
```sh
ffmpeg -framerate 10 -i Theta.%04d.jpeg -c:v libx264 -pix_fmt yuv420p Theta.mp4
```

- 视频横向合并
```sh
ffmpeg -i Theta.mp4 -i C.mp4 -filter_complex "[0:v]scale=1024:4096[v0]; [1:v]scale=1024:4096[v1]; [v0][v1]hstack=inputs=2" QPF.mp4
```
