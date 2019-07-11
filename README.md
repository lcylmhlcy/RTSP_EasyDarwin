# RTSP_EasyDarwin
> The video file in dav format is cyclically pushed to the streaming server EasyDarwin through the RTSP protocol.
  
**The whole file, please download from [BaiduYun](https://pan.baidu.com/s/1D478JwcfavC9H8Hp58r7wA) password：9a7z**
  
## How to use
1. Open the streaming server. Execute the bat file in the figure:
    <p>
      <img src="https://github.com/lcylmhlcy/RTSP_EasyDarwin/raw/master/img/1.png" width=600>
    </p>
    
    After success, as shown:
    <p>
      <img src="https://github.com/lcylmhlcy/RTSP_EasyDarwin/raw/master/img/2.png" width=600>
    </p>
2. Use ffmpeg to push the stream. Copy the video file to dir "video", as shown in the figure:
    <p>
      <img src="https://github.com/lcylmhlcy/RTSP_EasyDarwin/raw/master/img/3.png" width=600>
    </p>
3. Run cmd, go to the video directory, then run the command:
    ```
    ffmpeg.exe -re -stream_loop -1 -i NVR_ch11_main_20181217164115_20181217164718.dav -vcodec copy -f rtsp -rtsp_transport tcp rtsp://10.11.133.16:4008/admin.sdp
    ```
    **Note: "NVR_ch11_main_20181217164115_20181217164718.dav" is the video file name. "10.11.133.16" is replaced by your ip or 127.0.0.1.**  
    After success, as shown:
    <p>
      <img src="https://github.com/lcylmhlcy/RTSP_EasyDarwin/raw/master/img/5.png" width=600>
    </p>
