# multi-web hosting using Dockerfile(docker)
<h2>step-1</h2> 
launched instance using AWS
<h2>step-2</h2>
copied public ip address and pasted in kiitty terminal for easy acess
<h2>step-3</h2>
installed required packages using this cammands

```
sudo hostnamectl set-hostname docker
sudo su -
timedatectl set-timezone Asia/Kolkata
yum update -y
yum install git docker  -y
systemctl start docker
systemctl enable docker
systemctl ststus docker
```
<h2>step-4</h2>
create directory and  inside create Dockerfile.

```
mkdir /sai
vim Dockerfile
```
```
from httpd
run apt update -y
run apt install wget unzip -y
run wget https://www.free-css.com/assets/files/free-css-templates/download/page295/yoga.zip
run unzip yoga.zip                                                                          
```
```
run bootstrap-restaurant-template/* /usr/local/apache2/htdocs/
docker run -dt --name=c5 -t -p 92:80 saikumarvalmiki/yogawebsite
```
press esc and shift+: wq
```
docker build -t saikumarvalmiki/finterwebsite  .
```
<h2>step-5</h2>
create directory and  inside create Dockerfile.

```
mkdir /kumar
vim Dockerfile
```
```
from nginx
run apt-get update -y
run apt-get install wget unzip vim -y
run wget https://www.free-css.com/assets/files/free-css-templates/download/page294/artxibition.zip
run unzip artxibition.zip
run cp -rvf 2125_artxibition/* /usr/share/nginx/html/
```
```
docker build -t saikumarvalmiki/artweb .
docker run -dt --name=c3 -t -p 91:80 saikumarvalmiki/artweb
```
<h2>step-6</h2>
create directory and  inside create Dockerfile.

```
mkdir /valmiki
vim Dockerfile
```
```
from httpd
run apt update -y
run apt install git unzip wget -y
run git clone https://github.com/bedimcode/responsive-website-restaurant.git
run cp -rvf responsive-website-restaurant/* /usr/local/apache2/htdocs/
```
```
docker build -t saikumarvalmiki/food .
docker run -dt --name=c4 -t -p 93:80 saikumarvalmiki/food
```
<h2>step-7</h2>
check the running and stopped containers

```
docker ps
docker ps -a
```



https://github.com/user-attachments/assets/337b7816-5318-4592-aeb3-0ee3f2cff075



