# sms
xstrive media server and super media server whith golang.

## Features
* modularization, expansibility
* high performance, easy deployment, cross-platform
* support rtmp 
* support http-flv
* support hls

## Build

```
git clone https://github.com/xsw9527/sms.git
cd sms  
./build.sh  
```

## Run
./bin/sms

##Push and play
#Push rtmp stream to sms
ffmpeg -r 30 -f avfoundation -i "0:0" -vcodec libx264 -s 320*240 -b:v 100k -preset ultrafast -acodec libvo_aacenc -f flv rtmp://127.0.0.1/live/test
#Play rtmp streams
ffplay rtmp://127.0.0.1/live/test
#Play hls streams
ffplay http://127.0.0.1:8080/live/test.m3u8
#Play flv streams
ffplay http://127.0.0.1:8081/live/test.flv



