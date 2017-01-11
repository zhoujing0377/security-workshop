# 准备工作
## Java JDK 7 install

This is a requirement for both ZAP and the vulnerable web application-bodgeit.

1.`java -version` to check the java JDK version
2.If the version is smaller than 1.7, please download and install Java JDK 7 form below link `http://www.oracle.com/technetwork/java/javase/downloads/jdk7-downloads-1880260.html` Go to "Java SE Development Kit 7u79" and download the right verion(mostly it is Mac OS X x64)

## bodgeit download

The BodgeIt Store is a vulnerable web application which is currently aimed at people who are new to penentration testing.

1.Clone the repo `https://github.com/psiinon/bodgeit`
2.install a servlet engine, like tomcat
3.`brew install tomcat`
4.Change the port from 8080 to 9999 `/usr/local/Cellar/tomcat/8.5.9/libexec/conf/server.xml` to change 8080 to 9999
5.`mv /usr/local/Cellar/tomcat/8.5.9/libexec/webapps/ROOT /usr/local/Cellar/tomcat/8.5.9/libexec/webapps/ROOT.bak`
6.`cp -r /Users/yangxuemin/REA-1form/Workshops/bodgeit-master/root /usr/local/Cellar/tomcat/8.5.9/libexec/webapps/ROOT`
7.`cd /usr/local/Cellar/tomcat/8.5.9/libexec` * `./bin/startup.sh`

## ZAP install
`https://github.com/zaproxy/zaproxy/wiki/Downloads`

## 步骤

Step1 手动对购物网站 `http://localhost:9999/` 进行安全测试，比如SQL injection, XSS等

Step2 ZAP 自动扫描网站
