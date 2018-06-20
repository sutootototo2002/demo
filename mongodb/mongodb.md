###关闭服务
sudo systemctl stop  mongodb.service
###打开服务
sudo systemctl start mongodb.service

### 创建管理员用户
    use admin
    db.createUser({user:"admin",pwd:"admin",roles:[{"role":"userAdminAnyDatabase","db":"admin"}]})
    
### 利用Robot3T 连接mongodb远程服务器
![](https://i.imgur.com/xTqtekc.png)

![](https://i.imgur.com/30Hp40D.png)