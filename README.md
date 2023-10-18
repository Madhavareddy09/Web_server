# Developing a Simple Webserver
name:Madhavareddy

id:23009929

Dept: AIML
# AIM:

Develop a webserver to display about top five web application development frameworks.

# DESIGN STEPS:

## Step 1:

HTML content creation is done

## Step 2:

Design of webserver workflow

## Step 3:

Implementation using Python code

## Step 4:

Serving the HTML pages.

## Step 5:

Testing the webserver
# PROGRAM:
```
from http.server import HTTPServer, BaseHTTPRequestHandler

content = """
<html>
<head>
<body>
<h1>Top Five Web Application Development Frameworks</h1>
</body>
</head>
</html>
class HelloHandler(BaseHTTPRequestHandler):
    def do_GET(self):
        print("Get request recieved")
        self.send_response(200)
        self.send_header('Content-type','text/html;charset=utf-8')
        self.end_headers()
        self.wfile.write(content.encode())

print("This is my webserver")
server_address = ('',80)
httpd = HTTPServer(server_address,HelloHandler)
httpd.serve_forever()
```
# OUTPUT:
![output](images/webserver1.png)
# RESULT:

The program is executed succesfully
