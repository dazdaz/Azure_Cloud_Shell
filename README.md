# Azure_Cloud_Shell

#### Recipe to download files quickly from Azure Cloud Shell using Python3 - Warning : no authentication
```
python -m http.server 9000
ssh -R 80:localhost:9000 serveo.net
# Open up port 9000 in portal
# Point browser to -> https://abcdef.serveo.net
```

#### Execute specific pre-programmed commands in the Azure Shell via a web browser with authentication
```
wget https://github.com/msoap/shell2http/releases/download/1.13/shell2http-1.13.linux.amd64.tar.gz
tar xvzf shell2http-1.13.linux.amd64.tar.gz
./shell2http -basic-auth admin:admin -port 9000 /date date /ps "ps aux" 1>/dev/null 2>/dev/null &
ssh -R 80:localhost:9000 serveo.net
# Open up port 9000 in portal
# Point browser to -> https://abcdef.serveo.net
```
