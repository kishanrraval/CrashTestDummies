# Requirements
* Android Studio with latest SDK build version on Linux platform
* Node.js module
	- ```curl -sL https://deb.nodesource.com/setup_8.x | sudo -E bash -```
	- ```sudo apt-get install -y nodejs```
* 2 Android devices

# Steps to execute the entire project
* Clone this repository ```git clone https://github.com/kishanrraval/CrashTestDummies.git```
* _Skip the next 2 steps and use apks provided in the [apks](https://github.com/kishanrraval/CrashTestDummies/tree/master/apks) folder if you do not want to build apk from source._
* Create and run (Install on an Android device) the android project for server from [Android_Server](https://github.com/kishanrraval/CrashTestDummies/tree/master/Android_Server). It acts as a audio+video transmission server of a single source.
* Create and run (Install on an Android device) the android project for client from [Android_Client](https://github.com/kishanrraval/CrashTestDummies/tree/master/Android_Client). It is the recipient of the live stream and displays the stream on screen with audio.
* Run server.js file in the [NodeJS_server](https://github.com/kishanrraval/CrashTestDummies/tree/master/NodeJS_server) folder.
	- Use ```node server.js``` command to start the signalling server listening for incoming connections.
	- This signalling server works as an intermediate entity which establishes the connection between the source and the recipient.
* Find IP address of the signalling server which would be needed for connection. Go through the following steps for finding IP address of the server
      	- Open terminal and type ```ifconfig``` in the terminal to find the value of IPv4.
* Open Server app and enter the IP address from the above result and **tap on connect button**.
	- You can see the incoming connection from node server's command prompt.
* Open Client app and enter the same IP address over there as well and **tap on connect button**.
* __You will now be able to see the live streaming from client application.__
	
# Future developments
* Conversion of single source to multiple source transmission for achieving overall functionality.
* Improvements in UI to make app deployable and user friendly.
* Adding login/authentication feature if needed.
* Adding analytics feature, which can be used for finding user behaviour on app for finding issues and changes required in the app.

