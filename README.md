Oneliner: curl -o - https://raw.githubusercontent.com/jerryzhao173985/deck_revealed/main/boot_videos/futurama/futurama_install.sh | bash -

All customization is in the futurama folder with martin mv

And more video customization include converting using ffmpeg:

``` 
ffmpeg -i /Users/jerry/Downloads/deck-startup-best.mp4 \                                                                  ✘
       -filter:v "scale='min(1280,iw)':min'(800,ih)':force_original_aspect_ratio=decrease,pad=1280:800:(ow-iw)/2:(oh-ih)/2" \
       -c:v vp9 \
       deck_startup.webm  
```
       
       
And resize to avoid too long in size:

```  truncate -s 1840847 deck_startup.webm  ```
