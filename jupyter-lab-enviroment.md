### 1. Setup jupyter lab
```
user@Azure:~$ pip install jupyterlab
user@Azure:~$ jupyter notebook --generate-config
Writing default config to: /home/user/.jupyter/jupyter_notebook_config.py
```
### 2. Enable ‘allow_remote_access’
```
update jupyter_notebook_config.py
c.NotebookApp.allow_remote_access = True
```

### 3. Start jupyter lab
```
user@Azure:~$ jupyter lab --no-browser   
    To access the server, open this file in a browser:
        file:///home/user/.local/share/jupyter/runtime/jpserver-668-open.html
    Or copy and paste one of these URLs:
        http://localhost:8889/lab?token=e346d022915a04f9ad6789597a5b72e7d985c3d29ce69b01
     or http://127.0.0.1:8889/lab?token=e346d022915a04f9ad6789597a5b72e7d985c3d29ce69b01
```
### 4. Login jupyter lab
```
Replace the host name of URL from 'localhost:8889' as 'ngrok host name'
i.e. https://dcf2-52-187-120-48.ngrok.io/lab?token=e346d022915a04f9ad6789597a5b72e7d985c3d29ce69b01
```

### 5. Visit jupyter lab via browser
