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
