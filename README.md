### whitecoin_release for whitenode
    raspberry pi 3b+ 1G RAM
    
    readme version : V0.1  
    date:  2020.1.22
    whitecoind version: whitecoind_last = v2.5.4.0-19-ge1cd7c0

1. whitecoind_last
2. whitecoind_last.sha512.sum
---
# Update whitecoind in whitenode by CLI
 *Please update to Whitecoin 2.5.4 for your Whitenode(raspbarry pi 3B+)*
### Use git update way (English):
1. $ ssh pi@your_raspberry_ip    //default password is "raspberry"
2. $ sudo apt -y git zip tmux
3. $ git clone https://github.com/xwchelp/whitecoin_release.git whitecoind_sync
4. $ cd whitecoind_sync/script
5. $ ./do_install_whitecoind.sh
6. $ Done All
7. $  In your explorer input url: https://your_raspberry_ip for check it.


### 使用gitclone下载安装(Chinese):
1. $ ssh pi@your_raspberry_ip    //树梅派矿机缺省密码 "raspberry"
2. $ sudo apt-get install -y zip git tmux
3. $ git clone https://github.com/xwchelp/whitecoin_release.git whitecoind_sync
4. $ cd whitecoind_sync/script
5. $ ./do_install_whitecoind.sh  
6. 安装完成,可以在 浏览器查看你的矿机,地址栏输入:  https://your_raspberry_ip  
7. 注意1: $是树梅派给的提示信息,不用输入, 第一行 //之后是注释,不用输入
        用拷贝粘贴的方法,避免输入错误.  
8. 注意2: 本方法建议有一定的电脑知识的朋友使用,或者看更详细的教程

---

# Use This scipt by Build WhiteNode Image and Using GUI update

1. In WhiteNode image build script, use this command, download script to image.
   only one line
   #wget https://raw.githubusercontent.com/xwchelp/whitecoin_release/master/script/install_script_to_whitenode_image.sh \
    && chmod +x install_script_to_whitenode_image.sh && ./install_script_to_whitenode_image.sh
    
2. Now, php GUI can call this script for update whitecoind:
  1. $cd ~/script_whitecoind
  2. $start_update.sh
  
#start_update.sh 返回值:
#0=有新版本,更新成功! (本地文件可以没有,没关系)
#1=版本一样, 无需更新
#2=下载校验和错误, 很有可能是源码错误,等待开发者更新
#3=内部错误,保留
#4=下载错误,网络错误,等一段时间再来尝试
#注释: 返回值 shell中使用$?获取,必须马上获取.


   




