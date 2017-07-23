# Requirements
* Android Studio with latest SDK build version on Linux platform
* Node.js module
	- ```curl -sL https://deb.nodesource.com/setup_8.x | sudo -E bash -```
	- ```sudo apt-get install -y nodejs```
* socket.io module in node.js
	- use ```npm install socket.io``` for installation in the folder of the file `server.js`

# Steps to execute the entire application

* Create and run (Install on an Android device) the android project for server from [Server_Android](https://github.com/kishanrraval/CrashTestDummies/tree/master/Server_Android). It acts as a audio+video transmission server of a single source.
* Create and run (Install on an Android device) the android project for client from [Client_Android](https://github.com/kishanrraval/CrashTestDummies/tree/master/Client_Android). It is the recipient of the live stream and displays the stream on screen with audio.
* Run server.js file through node module.
	- Use ```node server.js``` command to run the signalling server.
	- This signalling server works as an intermediate entity which establishes the connection between the source and the recipient.
* Find IP address of the signalling server which would be needed for connection. Go through the following steps for finding IP address of the server
      	- Open terminal in the same PC in which the server is running.
      	- type ```ifconfig``` in the terminal and find value of IPv4. Which will be used in future for connection.
* Open Server android app and enter the IP address from the above result and **tap on connect button**.
	- You can see the response from node server's command prompt. (There won't be any response in case of improper connection).
* Open Client application and enter the same IP address over there as well and **tap on connect button**.
	- You will be able to see live streaming from server application. 
	
# Future steps
* Conversion of single source to multiple source transmission for achieving overall functionality.
* Improvements in UI to make app deployable and user friendly.
* Adding login/authentication feature if needed.
* Adding analytics feature, which can be used for finding user behaviour on app for finding issues and changes required in the app.

