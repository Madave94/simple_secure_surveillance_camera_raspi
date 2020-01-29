# Raspberry PI simple surveillance camera using TLS

This server sends a .mjpg stream to the specified ports. There are three different versions of the server.

1. [Implementation from the raspberry pi camera doc](https://picamera.readthedocs.io/en/release-1.13/recipes2.html#web-streaming)
2. [Only encrypted version without password, for testing purposes](https://github.com/Madave94/simple_secure_surveillance_camera_raspi/blob/master/EncryptedHTTPSServer.py)
3. [Version with encryption and password](https://github.com/Madave94/simple_secure_surveillance_camera_raspi/blob/master/AuthAndEncryptedHTTPSServer.py)

## How to run

You need to connect a raspberry pi camera (CSI).

For 2. and 3. it is nessecary to create the self-signed certificate first. When creating the certificate in the same folder use:
```
openssl req -new -x509 -keyout server.pem -out server.pem -days 365 -nodes
```
## Change login credentials

In script 3. at line 110 and 111 you can find the password and username used for login.

Credits to [simple-https-server](https://gist.github.com/dergachev/7028596).
