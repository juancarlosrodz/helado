var http = require("http");
var port = 9000;
  //incoming msg and response func fro the server
http.createServer(function (req, resp) {
    console.log(req.url);
    switch (req.method) {
        case "GET":
            if (req.url === "/") {
               
                resp.writeHead(200, { "Content-Type": "text/html" });
                //request to order icecream
                resp.write("<html><head><title>Hello User </title></head><body>Want to order icecream? Click <a href='/calc'>here</a></body><html>");
                resp.end();
            }
            break;
        case "POST":
            break;
        default:
            break;
    }
   
} 
).listen(port);
