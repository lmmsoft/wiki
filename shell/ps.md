> ps aux

```
USER       PID %CPU %MEM    VSZ   RSS TTY      STAT START   TIME COMMAND
root         1  0.0  0.6 225632  5824 ?        Ss   Feb09   4:27 /lib/systemd/systemd --system --deserialize 38
azureus+  3014  0.5 24.6 986796 230688 pts/1   Sl+  May01  24:06 python3.11 main.py
999      18655  0.5  8.3 1667768 78520 ?       Ssl  Feb15 607:54 mongod --auth --bind_ip_all
```

如图

python3.11 main.py (钉钉机器人) 用了 230mb 内存，占比 24% ，机器共 1G 内存

mongod (mongodb in docker) 用了 78M 内存， 占比 8.3%

Here's an explanation of each column in the ps output:
- USER: The username of the user that owns the process.
- PID: The process ID of the process. This is a unique number used to identify a running process.
- %CPU: 单核CPU占比 Percentage of CPU time used by the process. A value of 1.0 means the process is using 100% of one CPU core. 
- %MEM: 总内存占比 Percentage of total system memory used by the process.
- VSZ: 虚拟内存 Total amount of virtual memory used by the process (in KB). Includes memory that has been swapped out.
- RSS: 常驻内存 Resident memory used by the process (in KB). Includes only memory that is physically in RAM. 
- TTY: The terminal associated with the process.
- STAT: Process status. D is uninterruptible sleep, R is running, S is sleeping, T is traced/stopped, Z is defunct/zombie.
- START: The start time of the process.
- TIME: Total CPU time used by the process. In the format HOURS:MINUTES:SECONDS.
- COMMAND: The command that launched the process.
So in summary, the ps command gives you information about the resources (CPU, memory) used by processes, their status, ownership, start time, and the command that launched them.
The ps output, along with tools like top, vmstat, and iostat are very useful for monitoring system resources and the processes that are consuming them on Linux systems.
