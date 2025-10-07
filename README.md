# GarminMusicSync-BridgeService
Bridge Application to respond to Garmin app MusicSync.

Written in Python, the app reads of a defined folder (in the .conf file) and responds to the Garmin app over defined port (also in the conf file)

Due to Garmin's restriction, we must use HTTPS even in local networks. You will need to create your own certificate and state the ip of the remote server. Use the example below:

  For users to customize:
  Replace the IP addresses with their own server IP(s). Example for a single server:

  ```openssl req -x509 -newkey rsa:4096 -nodes -keyout bridge-key.pem -out bridge-cert.pem -days 10950 -subj "/CN=YOUR_SERVER_IP" -addext "subjectAltName=IP:YOUR_SERVER_IP,IP:127.0.0.1,DNS:localhost"```


Run clean for production use

Run debug for troubleshooting
