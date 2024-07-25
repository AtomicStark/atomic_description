1. node server :
     功能： 节点服务商，处理各种业务，加锁，解锁，获取订单信息然后处理。
     
3. relay server: 中间转发服务器 ，负责和Mysql服务器进行数据交互。
  
4. atomic_adapp:react 前端项目，负责 atomic stark 交互。

build :
  1. 在atomic_dapp 文件夹下，使用Npm run build 生成build文件，把build文件放到relay 服务器。
  2. relay_server 文件夹 替换relayServer后在服务器（45.32.100.53）路径 /root/atomic_dapp/depoly/relayServer/server 启动
  3. node_server 放到/root/atomic_dapp/depoly/nodeServer 文件夹下
     
启动：
 1. 在项目文件夹 /root/atomic_dapp/depoly/nodeServer pm2 start client.js
 2. 在文件夹 /root/atomic_dapp/depoly/relayServer/server/ pm2 start relay.js
