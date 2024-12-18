# podsys-monitor
**Monitor the deployment progress of podsys**

## Build

### create env
``` shell
# Create a minimal Python environment.
pip install Flask
pip install pyinstaller
```
``` shell
apt install upx


``` shell
pyinstaller --onefile --add-data "templates:templates" --add-data "static:static" --upx-dir=/usr/bin/upx --strip --clean --name podsys-monitor --exclude-module wheel --exclude-module PyGObject --exclude-module pyinstaller --exclude-module pipdeptree app.py
```
