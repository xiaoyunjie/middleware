# Middleware

middleware 组件仓库，用于记录部署、配置、规范等。


## 放行iptables
```bash
# nacos
firewall-cmd --zone=public --add-port=8848/tcp --permanent
firewall-cmd --zone=public --add-port=9848/tcp --permanent
firewall-cmd --zone=public --add-port=9849/tcp --permanent
# nacos-mysql
firewall-cmd --zone=public --add-port=3306/tcp --permanent
# redis
firewall-cmd --zone=public --add-port=6379/tcp --permanent
# minio
firewall-cmd --zone=public --add-port=9000/tcp --permanent
firewall-cmd --zone=public --add-port=9001/tcp --permanent

# 软加载
firewall-cmd --reload
```

## 运行

docker-compose up -d
