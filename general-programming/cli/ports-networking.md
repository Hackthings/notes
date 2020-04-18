# Ports / Networking

Find my network IP address  
**`ipconfig getifaddr en0`** 

Find and kill what's blocking a port:  
**`kill -9 $(lsof -i TCP:8000 | grep LISTEN | awk '{print $2}')`** 




