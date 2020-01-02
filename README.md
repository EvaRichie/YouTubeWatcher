# Find & Download YT vids as mp3/mp4

- experiment with UWP and see what it can do 
- test the folder/file/security/permission uwp api
- experiment on the media api's & controls to see how evolved the uwp api is
- use 3rd party libs , ffmpeg / youtubeconverter. Lets see how easy it is to incorporate them in the UWP sandbox
- use sqlite for client side DB persistence


Home (webview loading youtube): 
![alt text](https://github.com/liquidboy/YouTubeWatcher/raw/master/Assets/1.PNG)

Youtube Selected Video (webview loading youtube video):  This gives you the option to download the vid as mp3/4 and quality
![alt text](https://github.com/liquidboy/YouTubeWatcher/raw/master/Assets/2.PNG "")

Job : once you download video it is queued as a job
![alt text](https://github.com/liquidboy/YouTubeWatcher/raw/master/Assets/3.PNG "")

Job : closer look at the taskbar showing inprogress job, job queue count and Library count
![alt text](https://github.com/liquidboy/YouTubeWatcher/raw/master/Assets/4.png "")

Library (clicking on library tile on taskbar) : clicking on library tile will take you to the Library (xaml view of the media you downloaded)
![alt text](https://github.com/liquidboy/YouTubeWatcher/raw/master/Assets/5.PNG "")

MediaPlayer above Webview: playing from your library will load the UWP MediaPlayerElement which has no airspace issues with webview, so appears above it.
![alt text](https://github.com/liquidboy/YouTubeWatcher/raw/master/Assets/6.PNG "")

Windows process : webview , Xaml UWP app (including media player), FFMpeg all run in separate processes all grouped underneath a parent process. This is mostly free, or very low amount of code required (1 line of code for webview).
![alt text](https://github.com/liquidboy/YouTubeWatcher/raw/master/Assets/7.PNG "")