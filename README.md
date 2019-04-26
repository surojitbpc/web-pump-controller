Installing Flask

We’re going to use a Python microframework called Flask to turn the Raspberry Pi into web server.
To install Flask, you’ll need to have pip installed. Run the following commands to update your Pi and install pip:

pi@raspberrypi ~ $ sudo apt-get update
pi@raspberrypi ~ $ sudo apt-get upgrade
pi@raspberrypi ~ $ sudo apt-get install python-pip python-flask

Then, you use pip to install Flask and its dependencies:

pi@raspberrypi ~ $ sudo pip install flask

Creating the Python Script:

This is the core script of our application. It sets up the web server and actually interacts with the Raspberry Pi GPIOs.
To keep everything organized, start by creating a new folder:

pi@raspberrypi ~ $ mkdir web-server
pi@raspberrypi ~ $ cd web-server
pi@raspberrypi:~/web-server $

Create a new file called app.py:

pi@raspberrypi:~/web-server $ nano app.py


Copy and paste the following script to your Raspberry Pi (this code is based on Matt Richardson great example).


Creating the HTML File

Keeping HTML tags separated from your Python script is how you keep your project organized.
Flask uses a template engine called Jinja2 that you can use to send dynamic data from your Python script to your HTML file.

Create a new folder called templates:

pi@raspberrypi:~/web-server $ mkdir templates
pi@raspberrypi:~/web-server $ cd templates
pi@raspberrypi:~/web-server/templates $


Create a new file called main.html:

pi@raspberrypi:~/web-server/templates $ nano main.html

Copy and paste the following template to your Pi:
