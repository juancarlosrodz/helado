var http = require("http");
var port = 9000;
  //incoming msg and response func fro the server
http.createServer(function (req, resp) {
    resp.writeHead(200, { "Content-Type": "text/html" });
    resp.write("<html><body>Hello <strong><i>World</i></strong></body><html>");
    resp.end();
}
).listen(port);
