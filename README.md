# Ex-01-Simple-Web-Server
## Date:

## AIM:
To develop a simple webserver to serve html pages.

## DESIGN STEPS:
### Step 1: 
HTML content creation.

### Step 2:
Design of webserver workflow.

### Step 3:
Implementation using Python code.

### Step 4:
Serving the HTML pages.

### Step 5:
Testing the webserver.

## PROGRAM:
```
from http.server import HTTPServer,BaseHTTPRequestHandler

content="""
<html>
<body>
<head>
<h1> The Top five Web Application Development Frameworks.</h1>
<h2>1.Django</h2>
<h3>2.MEAN Stack</h3>
<h4>3.React</h4>
<h5>4.Ruby on Rails
<h6>5.Angular</h6>
</body>
</head>
</html>
class HelloHandler(BaseHTTPRequestHandler):
    def do_GET(self):
        self.send_response(200)
        self.send_header('Content-type','text/html;charset=utf-8')
        self.end_headers()
        self.wfile.write(content.encode())

print("Welcome To The Sai Ganesh Webpage")
server_address=('',80)
httpd=HTTPServer(server_address,HelloHandler)
httpd.serve_forever()
```
## OUTPUT:
![WhatsApp Image 2023-11-22 at 10 40 49_1587606d](https://github.com/mohammadshahil09/ODD2023-WT-Ex-01-Simple-Web-Server/assets/145742840/406fb62e-669f-4bde-ac49-33c69cdbe23d)


## RESULT:
The program for implementing simple webserver is executed successfully.
