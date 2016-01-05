# cordova-chrome-video-audio-test
Test cordova project which shows off bug in Chrome which disables background audio for muted videos.

### Install cordova
```
sudo npm install -g cordova
```

### Create Cordova app
```
cordova create hello-video-audio com.example.hello HelloWorld
cd hello-video-audio
```

### Add Android platform
```
cordova platform add android
```

I set my AndroidManifest.xml to target android:targetSdkVersion="21" and project.properties to target=android-21

### Build Android project

```
cordova build
```

### Installing Cordova HTML5Video plugin for showing video inline on Android
```
cordova plugin add https://github.com/jaeger25/Html5Video.git
```

Next I updated www assets to add html and js and added mp4 videos to platforms/android/res/raw directory

### Tested app works on a physical device
```
cordova run android
```


- Notice that the background music will stop after 3000ms when the video begins playing

- If you would like to test a shorter video, swap out the `initializeVideo` functions in `onDeviceReady`
