Install mysql on windows with default root password welcome

login to mysql shell :

mysql.exe -u root -p

create the db using the db.sql script in the repo (copy paste into mysql shell)

Install node.js on windows and clone this repo

git clone https://github.com/n-mam/foxpad.git

change directory in the cloned repo folder and issue :

"npm install" from the repo root folder

"npm start" from the repo root folder

use e1/e1, e2/e2 or e3/e3 to login to the app

at this point you'd also need the agent running on the system. 

This can be downloaded from http://52.66.251.154:8080/ home page "Download Agent" button. 

test setup should be up and running at this point

The frontend UI makes use of https://metroui.org.ua/ for UI controls and https://www.chartjs.org/for reporting

# do not use the below instructions

download mysql zip file for windows

type c:\windows\my.cnf

[mysqld]
basedir=C:\\code\\mysql-8.0.20-winx64
datadir=C:\\code\\mysql-8.0.20-winx64\\data

mysqld --initialize --console

note the initial password:

[Note] [MY-010454] [Server] A temporary password is generated for root@localhost: L=Vxv)Oqw5oa

ALTER USER 'root'@'localhost' IDENTIFIED BY 'welcome';

ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'welcome';

flush privileges;
-----

The agent also requires the below setup on the machine

download and install cuda toolkit 

download and unzip cudnn

Copy the following files into the CUDA Toolkit directory.
Copy <installpath>\cuda\bin\cudnn*.dll to C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\vx.x\bin.
Copy <installpath>\cuda\include\cudnn*.h to C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\vx.x\include.
Copy <installpath>\cuda\lib\x64\cudnn*.lib to C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\vx.x\lib\x64.