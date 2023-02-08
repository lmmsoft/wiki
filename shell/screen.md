# screen 命令比较
- 2019-02-25 今晚学习了 screen 命令，用于在远程ssh上执行程序，不被网络断开影响，而且还能在断开之后回到过去的命令
* 查询
    * screen -ls
    * screen —list
* 创建
    * screen -S foo
* 连接 detached状态的 screen
    * screen -r 12345 # 后面数字是screen -list 里面的pid
* 连接 attached状态的 screen
    * screen -rd 12345 # 后面数字是screen -list 里面的pid
* 跳出当前窗口，并不退出
    * Ctrl+a d
    * Ctrl+a k  (kill current)
* screen -X -S [session # you want to kill] quit
    * kill detached session
* screen -x
    * attaches to a running session without detaching from its current attachment. This argument is especially useful when you and another user are trying to access the same session at the same time
* Ctrl+a ? 
    * Will display a list of all the command options available for Screen.
    * 先按 Ctrl + a (Mac也是control) 再单独按 ? (即 Shift+ / (?) )
* ssh -t <user>@<server> screen -r
    * When connecting to a remote session via SSH it is best to connect with Screen at the same time. The syntax is as follows:
* 检查是否在screen里面
    * echo $STY
    * echo $TERM
* https://www.ibm.com/developerworks/cn/linux/l-cn-screen/
* http://pkuwwt.github.io/linux/2013-12-04-gnu-screen-an-introduction-and-beginners-tutorial/
    * GNU Screen--介绍和初学者指南[译]
