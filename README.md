# SpeechAPIDemo
JAVA application demonstrating the use of the net-speech-api for kaldigstserver.


Large parts of the code are based on https://github.com/Kaljurand/net-speech-api, and this code 
can be used as a starting point for a client using kaldigstserver (https://github.com/alumae/kaldi-gstreamer-server).

You can compile this program using:

`$ mvn package`

Alternatively, you can use the provided .zip to get the same result.

Run the application using:

`$ java -jar target/SpeechAPIDemo-1.0.jar server:port [userid] [contentid]`

The server is assumed to be running on ws://server:port/client/ws/speech, with status info on ws://server:port/client/ws/status.

The main screen contains 2 buttons. Use 'Select File' to transcribe speech from a file. This can be in any format that is supported by the server. Use 'Start Live Recognition' to transcribe from a microphone, using the 'Opus Compression' pulldown menu, you can apply compression to the (live) speech signal, in order to save bandwidth. In 'live' mode, a bar on the top right indicates sound level. If that is lighting up without you speaking, or not showing anything, there may be something wrong with your microphone setup. If it is regularly showing red, it would be wise to reduce the recording level.

The results part has 2 tabs: txt and ctm. The former shows the standard textual output, whereas the latter gives you results in .ctm format. Right-clicking on the results pane allows you to save the output.
