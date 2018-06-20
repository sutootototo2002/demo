###关闭服务
sudo systemctl stop  mongodb.service
###打开服务
sudo systemctl start mongodb.service

### 创建管理员用户
    use admin
    db.createUser({user:"admin",pwd:"admin",roles:[{"role":"userAdminAnyDatabase","db":"admin"}]})
    
