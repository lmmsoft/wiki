# 常用命令

## kill by port 

- Find the process using port 8080:

  sudo lsof -i:8080


- Kill the process on that port:

  kill $PID
  kill -9 $PID  //to forcefully kill the port

PID is got from step 1's output.
