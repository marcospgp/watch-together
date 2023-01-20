# Watch Together

Notice: This project was deprecated in 2015 and will no longer be maintained.

A Chrome extension that allows multiple users to synchronize their streams on a popular streaming
service, making use of an intermediary Node.js server for peer to peer communication.

Users join a room by name and their stream will automatically be synchronized with others in that
room. If one pauses the player, everyone has their stream paused, and so on.

## How it works

* The streaming service uses an iframe to serve the video player;
* This extension accesses the page inside the iframe and interacts with the video player object
present in the `window` object;
* This is done by injecting a script into the pages being rendered inside the iframe and giving that
script access to the chrome communication api;
* This means the script can react to events in the video player and is able to communicate with the
rest of the extension, which manages synchronization between the different users.
