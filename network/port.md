# how to kill a process running on a port

## 1. open cmd

## 2. use netstat command
netstat -ano|findstr "PID :4000"
Proto Local Address Foreign Address State PID
TCP 0.0.0.0:4000 0.0.0.0:0 LISTENING 8152

## 3. kill the process (the /f is force):
taskkill /pid 18264 /f

<https://community.talend.com/t5/Architecture-Best-Practices-and/How-to-find-and-kill-a-process-running-on-a-port/ta-p/55315>