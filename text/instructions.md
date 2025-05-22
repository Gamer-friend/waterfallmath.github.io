## >>SERVER INSTRUCTIONS START<<

First, go to the top of the repo (on the `Server` branch) and click on code > codespaces > create codespace
now you have your own free server instance to host eaglercraft. Next you need to run the setup commands:

create 2 terminal tabs and paste in the following snipits:

first terminal: `cd server && sudo java -jar server.jar`

second terminal: `cd bungee && sudo java -jar bungee.jar`

Now go to the ports area and forward (and make public) ports 25565 and 8081

And then, ⚠ MOST IMPORTANT! ⚠
Copy the 8081 port address and it should be like, for example, `https://eagtek-files-392jejdw-8081.app.github.dev` . Copy this and paste it in your ⚠⚠⚠ browser BUT DONT,  ⚠⚠⚠⚠ DO NOT PRESS `ENTER` YET!⚠⚠⚠⚠ 
Instead, replace the `https` (in the beginning of the port address) and replace it with a `wss` . Here is some examples:
❌ WRONG: `https://eagtek-files-392jejdw-8081.app.github.dev`
✅ CORRECT: `wss://eagtek-files-392jejdw-8081.app.github.dev`

Be sure that it is in `public` mode, edit the `index.html` file in the `Main` (the default) Branch. You may need to also CHANGE THE ADDRESSES IN THE `eaglersecure.html` file, like in my repository, [here](https://github.com/Gamer-friend/googlecom/blob/main/eaglersecure.html)
Since it is too large, download the file, edit it, and REUPLOAD IT.

Thats it, your done! Enjoy!!!
