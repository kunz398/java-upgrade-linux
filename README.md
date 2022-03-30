
# java-upgrade-linux
upgrading of java version to 1.8.0_311 in Oracle Linux / Red Hat / CentOS


1. download: jdk1.8.0_311 from here 

> https://www.dropbox.com/s/xb59rbkttdch9q1/jdk-8u311-linux-x64.rpm?dl=0

2. Transfer the file in your linux system and do installation.
	
     

3. cd to the directory its stored in my case its in downloads and install the rpm package
     ``
     cd /home/kunz/Downloads/   
     ``
     
     ``
      rpm -i jdk-8u311-linux-x64.rpm
      ``
4. next confirm if installation has taken place

 
`` $ cd /usr/java``
`` $ ll`` 
 ``drwxr-xr-x  9 root root 4096 Feb  1 21:47 jdk1.8.0_311-amd64``

> the above shows i have installed version _311 now we need to set up
> the environment variables.

this will print out all env variables relating to java
   

      $ printenv | grep java
      PATH=/usr/java/jdk1.8.0_181-amd64/bin:/usr/local/bin:/usr/bin:/usr/local/sbin:/usr/sbin:/home/kunz/.local/bin:/home/kunz/bin PWD=/usr/java 
      JAVA_HOME=/usr/java/jdk1.8.0_181-amd64

> in my case i had to change the env variable from version 181 to
> version 311

    export PATH=usr/java/jdk1.8.0_311-amd64/bin:/usr/local/bin:/usr/local/sbin:/usr/bin:/usr/sbin:/bin:/sbin:/home/kunz/.local/bin
    export JAVA_HOME=/usr/java/jdk1.8.0_311-amd64

> check the env varible again

    $ printenv | grep java
      PATH=/usr/java/jdk1.8.0_311-amd64/bin:/usr/local/bin:/usr/bin:/usr/local/sbin:/usr/sbin:/home/kunz/.local/bin:/home/kunz/bin
    PWD=/usr/java
    JAVA_HOME=/usr/java/jdk1.8.0_381-amd64

> should have now changed to 311
next check java version


    $ java -version
    openjdk version "1.8.0_311"
    OpenJDK Runtime Environment (build 1.8.0_311-b06)
    OpenJDK 64-Bit Server VM (build 25.311-b06, mixed mode)
    $
