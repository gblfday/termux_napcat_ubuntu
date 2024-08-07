为napcat做的termux恢复包
- 内置napcat=1.7.7/linuxqq=3.2.9/nonebot2=2.3.2
- 建议恢复后，自己更新以上程序，nc和linuxqq直接下载最新版覆盖即可，nonebot2就更新py包：pip install -U nb-cli 如果未能更新请输入：pip install --upgrade nb-cli

##启动proot容器
- cd ubuntu-in-termux
- ./startubuntu.sh

##开启bot
首先先开启两个会话窗口来启动nb和nc
- screen -S nb   ##这里先开一个窗口然后启动nb：nb run --reload 然后退出当前会话：ctrl+a再输入D 回到住窗口。
- screen -S nc   ##这里再启动一个窗口来启动nc：./run.sh 然后输入各种信息，再输入ctrl+a再输入D，回到住窗口。
- 如何切换会话窗口：↓
- screen -ls   ##这里是显示你现在所有会话窗口！
- screen -r xx   ##这里是切换到已有的会话窗口如：screen -r nb就进入到我们已经刚刚创建的窗口！
- 要关闭容器直接输入exit(),或者ctrl+c 即可关闭当前窗口，如果当前会话正在有程序在运行，则会先关闭程序，需要再输入才关闭此窗口！
