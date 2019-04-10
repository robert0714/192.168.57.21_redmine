# 192.168.57.21_redmine
正式機正式指令


```bash
docker run --name=redmine -d --publish=10080:80 \
  --env='REDMINE_RELATIVE_URL_ROOT=/redmine' \
--env='SMTP_USER=iisi.sonar@gmail.com' --env='SMTP_PASS=0920301309' \
 -e  "TZ=Asia/Taipei" \
 -e "DB_TYPE=postgres" -e "DB_HOST=192.168.57.21" \
  -e "DB_NAME=redmine" -e "DB_USER=redmine" -e "DB_PASS=redmine" \
  --volume=/mnt/repos/redmine/data:/home/redmine/data \
  sameersbn/redmine:3.0.3

```

```bash
docker run --name postgresql -itd --restart always \
  --publish 5432:5432 \
  --volume /mnt/repos/postgresql/9.4/data:/var/lib/postgresql \
  sameersbn/postgresql:9.4-4 
  
 ```
