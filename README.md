# azure-cloud-shell-developing-environment <br>
### 1. Login github
```
user@Azure:~$ gh auth login
- What account do you want to log into? GitHub.com
- What is your preferred protocol for Git operations? HTTPS
- Authenticate Git with your GitHub credentials? Yes
- How would you like to authenticate GitHub CLI? Login with a web browser

! First copy your one-time code: XXXX-XXXX
Press Enter to open github.com in your browser...
! Failed opening a web browser at https://github.com/login/device
  exec: "xdg-open,x-www-browser,www-browser,wslview": executable file not found in $PATH
  Please try entering the URL in your browser manually
✓ Authentication complete.
gh config set -h github.com git_protocol https
✓ Configured git protocol
 Logged in as userid
user@Azure:~$
```
### 2. Clone the Repository
user@Azure:~$ git clone https://github.com/your_id/your_project.git<br>

### 3. Setup ngork
- Download ngrok & Unzip
```
user@Azure:~$ wget 'https://bin.equinox.io/c/4VmDzA7iaHb/ngrok-stable-linux-amd64.zip' -O ngrok.zip
user@Azure:~$ unzip ngrok.zip
```
- Get ngrok token from https://dashboard.ngrok.com/get-started/your-authtoken<br>
```
user@Azure:~$ ./ngrok authtoken 'your token'
Authtoken saved to configuration file: /home/user/.ngrok2/ngrok.yml
```
- Start ngrok http <port#>
```
user@Azure:~$ ./ngrok http 8889
ngrok by @inconshreveable                                                                                                                                                                          (Ctrl+C to quit)
                                                                                                                                                                                                                   
Session Status                online                                                                                                                                                                               
Account                       yourid (Plan: Free)                                                                                                                                                                
Version                       2.3.40                                                                                                                                                                               
Region                        United States (us)                                                                                                                                                                   
Web Interface                 http://127.0.0.1:4040                                                                                                                                                                
Forwarding                    http://0200-52-187-120-48.ngrok.io -> http://localhost:8889                                                                                                                          
Forwarding                    https://0200-52-187-120-48.ngrok.io -> http://localhost:8889                                                                                                                         
                                                                                                                                                                                                                   
Connections                   ttl     opn     rt1     rt5     p50     p90                                                                                                                                          
                              0       0       0.00    0.00    0.00    0.00  
```
