# rpm-maven-plugin-apache-tomcat-packaging
Can the rpm-maven-plugin be used to package tomcat rpm? Need a Jenkins on RHEL or CENTOS. YES IT CAN!!!

# RPM repackage of tomcat distribution ZIP file

Proving ground to see if maven rpm plugin can be used.

* Download package
* Jenkins Master
* RPM LINUX (Centos) VM
* Jenkins Slave on Centos
* Maven Project 
* Jenkins Job to build project

This project depends on and extends the [Deployment Pipeline](https://github.com/lastnitescurry/j2ee-rest-jersey-jetty-tomcat-maven-jenkinsfile#deployment-pipeline) tools
 
## Get host ip for VM

	netstat -rn

* http://superuser.com/questions/310697/connect-to-the-host-machine-from-a-virtualbox-guest-os

## Maven Plugin

* http://www.mojohaus.org/rpm-maven-plugin/example1.html
* https://thejiraguy.wordpress.com/2013/12/17/deploying-jira-in-the-enterprise-part-2-packaging-using-the-rpm-maven-plugin
* https://books.sonatype.com/nexus-book/reference/yum-example-usage.html#yum-rpm-pom

## TEST 
#### Install

	sudo yum --assumeyes install target/rpm/apache-tomcat/RPMS/noarch/apache-tomcat-8.5.4-1.noarch.rpm

#### UnInstall

	sudo yum --assumeyes erase apache-tomcat
