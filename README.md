# 作業環境を用意
https://github.com/zukaishi/terraform/tree/main/workspace

# ec2_-docker
sudo yum clean all<br>
<br>
sudo yum update -y<br>
<br>
sudo amazon-linux-extras install docker <br>
<br>
sudo service docker start<br>
<br>
sudo usermod -a -G docker ec2-user<br>
<br>
一度EC2からログアウト、再度SSH接続する<br>
<br>
docker info<br>
<br>
docker login<br>
<br>
vim index.html<br>
```
hello
```

vim dockerfile<br>
```
FROM centos:latest  
RUN yum install -y httpd
COPY ./index.html /var/www/html/index.html
EXPOSE 80 443
CMD ["/usr/sbin/httpd", "-D", "FOREGROUND"]
```
docker image build -t dockerdemo ./<br>
docker image ls<br>
docker run -d -p 8080:80 dockerdemo:latest<br>
<br>
ブラウザアクセス<br>
https://[_ip address_]:8080<br>
<br>
docker network ls<br>
docker network inspect bridge<br>
<br>
docker container ls<br>
docker container inspect [_container_id]
docker container ps<br>
<br>
docker container stop [CONTAINER ID]<br>