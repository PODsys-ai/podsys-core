# podsys-monitor
**Monitor the deployment progress of podsys**

## Build in Docker(recommend)
** The size of the packaged file is smaller using this method **
### Create container
``` shell
docker run --name podsys-monitor-build --privileged=true -it -p 5000:5000 -v D:/podsys-monitor:/root/podsys-monitor  ubuntu:22.04 /bin/bash
```
### install env in container
``` shell
apt update
apt install python3
apt install python3-pip
apt install upx
pip install Flask
pip install psutil
pip install pyinstaller
cd /root/podsys-monitor
```

### build
``` shell
pyinstaller --onefile --add-data "templates:templates" --add-data "static:static" --upx-dir=/usr/bin/upx --strip --clean --name podsys-monitor --exclude-module wheel --exclude-module PyGObject --exclude-module pyinstaller --exclude-module pipdeptree app.py
```