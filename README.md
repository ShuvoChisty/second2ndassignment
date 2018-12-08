npm init command created  a package.json file.

After this we have install these package by giving following command:
    npm install --save express
    npm install --save mongoose
    npm install --save body-parser
    
which will used to listen to the server.

app.get('/', function(req, res){
  res.sendFile(__dirname + '/index.html');
});
this is oue send file....i have used.
***.............................................
npm install --save socket.io
During development, this socket.io serves the client automatically for us, as we’ll see, so for now we only have to install one module:

**.......................................
http.listen(3000, function(){
  console.log('listening on *:3000');});
  
 this command will create a new instance of socket.io by passing the http (the HTTP server) object. Then I listen on the connection event for incoming sockets, and I log it to the console.
...............................................
Now in index.html I add the following snippet before the </body>:

<script src="/socket.io/socket.io.js"></script>
<script>
  var socket = io();
</script>

That’s all it takes to load the socket.io-client, which exposes a io global, and then connect.

Notice that I’m not specifying any URL when I call io(), since it defaults to trying to connect to the host that serves the page.
.........................
The main idea behind Socket.IO is that can send and receive any events you want, with any data you want. 

And on the client side when we capture a chat message event we’ll include it in the page. The total client-side JavaScript code now amounts to..