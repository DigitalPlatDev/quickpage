# QuickPage
Quickly create and share HTML pages, support Bootstrap 5. Generate your own URLs for quick page sharing  
Click STAR to support our development  
Sponsor us: [Patreon](https://www.patreon.com/xingyujie)  [PayPal](https://paypal.me/xingyujie50)
## Get community support
[Telegram](https://t.me/digitalplatdev)  
[Discord](https://discord.gg/xhZhjcZd)  
[Follow us on Twitter for the latest news and updates](https://twitter.com/digitalplatdev)  
# Quick start
Demo: https://quickpage.digitalplat.org  
System Requirements: Linux, Windows or Unix-like System  
Python requirements: Python 3.7+  
## Install Python
### On Linux systems:
Debian-like system: `apt update & apt install python3 python3-pip -y`  
CentOS-like system: `yum update & yum install -y python3 python3-pip`  
For other Linux distributions, please Google :D
### On Microsoft Windows
Go to https://www.python.org/downloads/ to download the latest Python releases  
In the first installation interface, be sure to check `Add Python3.xx to PATH`
## Install library
Enter Linux BASH or Windows CMD  
If you have Git, you can use `git clone https://github.com/xingyujie/quickpage.git`  
If you don't have Git, click `Code -> Download ZIP` in the Github repository and unzip it  
Change to the working directory, e.g. `cd quickpage-main`
Check if you are in the root directory of the quickpage source and use `pip install -r requirements.txt` and wait for installation  
## Start server
If everything is in order, then you can start the server...  
Make sure you are still in the working directory  
### Change the gevent configuration file start.py to configure the listening address and port 
Open the `start.py` file (in the working root directory) with any editor such as `vim`, `mousepad`, `vscode`, and you will see the following code  
```
from gevent.pywsgi import WSGIServer
from main import app

http_server = WSGIServer(("0.0.0.0", 5400), app)
http_server.serve_forever()
```
`0.0.0.0` is the listening address, `5400` is the listening port, usually we only need to change the listening port  
