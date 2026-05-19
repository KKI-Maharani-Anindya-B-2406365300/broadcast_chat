## Experiment 2.1: Original code of broadcast chat

**How to run it:**
To get this chat application working, I had to run the server and the clients separately. First, I opened a terminal and started the server using the command 'cargo run --bin server'. Then, I opened three terminal windows and ran 'cargo run --bin client' in each one to simulate three different users connecting to the chat room.

**What happens when you type text:**
When I type a message into one of the client terminals and press Enter, that message is sent over a WebSocket connection to the server. As shown in the server screenshot, the server registers the new connections and logs the incoming messages (like "hello", "hellooo", and "helloooooo") along with the IP address and port of the sender. The server then acts as a central hub, taking that message and broadcasting it out to all the other connected clients so everyone in the chat can see it.

![alt text](image.png)