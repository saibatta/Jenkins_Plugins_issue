### **Jenkins Installation**

To Install the Jenkins need to follow the below steps 

1.  Install Java V8 or V11 – Jenkins is a Java based application, hence Java is a must.

       a. install the [JDK(v11)](https://www.oracle.com/in/java/technologies/javase-jdk11-downloads.html) from this link.

       b. add JDK path in environment(system) variables
                    
        variable name : JAVA_HOME  
        variable value: C:\Program Files\Java\jdk-11.0.11
        variable name : Path  (Path will be available as a default so just add variable value)
        variable value: C:\Program Files\Java\jdk-11.0.11\bin
       
       c. now check the `java -version` from the command line and if it return below lines then java installed successfully       
               
        java version "11.0.11" 2021-04-20 LTS
        Java(TM) SE Runtime Environment 18.9 (build 11.0.11+9-LTS-194)
        Java HotSpot(TM) 64-Bit Server VM 18.9 (build 11.0.11+9-LTS-194, mixed mode)

2.  Install  Jenkins
         
       a. download [Jenkins(windows .msi file)](https://www.jenkins.io/download/thank-you-downloading-windows-installer-stable) from this link 
       
       b. check [this link](https://www.jenkins.io/doc/book/installing/windows/) to step by stem installation of the MSI installer in windows machine 
  

### Plugin installation issue 
if you are unable to install the Jenkin plugins due to the below error
       
       Jenkins sun.security.provider.certpath.SunCertPathBuilderException: unable to find valid certification path to requested target

then stop the Jenkin service from the **Windows Service** and download the [skip-certificate-check.hpi](https://updates.jenkins.io/download/plugins/skip-certificate-check/1.0/skip-certificate-check.hpi) in Jenkins Plugin directory 

> C:\Windows\System32\config\systemprofile\AppData\Local\Jenkins\.jenkins\plugins

now restart the Jenkins service from the Windows Service and then install the necessary plugin from the **Jenkins Plugin manager**
