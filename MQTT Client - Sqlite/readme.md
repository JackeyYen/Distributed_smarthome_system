# 代码内容包含：

    MQTT通信客户端和创建模拟数据库代码：
        mqttsubclient_nogateway.py
        mqttsubclient.py
        mqttpubclient.py

# 使用说明：

    树莓派上操作：
       将代码拷贝至已经配置好环境的树莓派中，执行.py程序文件
       mqttpubclient.py与mqttsubclient.py都执行
       若是使用Arduino作为节点测试，订阅端程序改成执行mqttsubclient_nogateway.py
       ex.
          - # python3 mqttpubclient.py
          
    用网关测试：
       确保树莓派与网关在同一局域网下
       透过串口连接工具进入网关
       执行
          - # python gateway_2_0.py 192.168.137.9 30
      （192.168.137.9是树莓派服务器IP地址，30表示采样周期为30s）

# 备注：

     备注1.
         启动并查看 MQTT Server 服务运行状态(正常情况下开机就会自动运行)
         在树莓派终端执行
         - # sudo service mosquitto start
         - # sudo service mosquitto status
         - # netstat -an | grep 1883
         
     备注2.
         使用python编写程序进行测试MQTT的发布和订阅功能要安装(树莓派上已安装)
         - # sudo pip3 install paho-mqtt
