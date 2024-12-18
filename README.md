# podsys-monitor
**Monitor the deployment progress of podsys**

``` shell
pyinstaller --onefile \
    --exclude-module tkinter \
    --exclude-module _tkinter \
    --add-data "templates:templates" \
    --add-data "static:static" \
    --name podsys-monitor \
    app.py
```
