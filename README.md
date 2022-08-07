# cordova-plugin-android-enumeratedevices

Experimenting with this to see if it is able to provide proper labels for android devices.  So far not providing useful enough information to be useful.  If anyone has a better solution, or has made this work, please let me know.

Cordova Android plugin exposing the audio and video devices connected


We develop this plugin with the aim of fix the empty devices labels in ionic Android using de android webview WebRTC API. We got the labels with the native code but the devices id's were quite different with the WebRTC API that the ionic webview provide us. This is why we were not able to joint the labels with the devices.

Inferring that the devices returned by WebRTC API and by the native code (plugin) arrive in the same order, we match the labels with the id's in the ionic app side.

Just calling to

`cordova.plugins.EnumerateDevicesPlugin.getEnumerateDevices().then(devices => console.log(devices));`
