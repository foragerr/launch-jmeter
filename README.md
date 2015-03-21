# run-jmeter-with-plugins-via-build-tools

A Maven project to run the latest Jmeter with all plugins included using a build tool like Maven or Gradle.

## How-To

To run, it requires you have Maven installed on your system.  Execute using the included .bat script 
on Windows.   If you want to run on Linux, just create a similar Bash script.

There are two different methods you can launch Jmeter with in this project:

- Run with Gradle option will run Jmeter version 2.6, which does not have support for the Selenium remote webdriver example I provide below - ```startJmeterWithGradle.bat```
- Run with Maven option will run Jmeter version 2.11 with plugins version 1.2.1, which does support the Selenium remote webdriver example I provide below - ```startJmeterWithMaven.bat```

When Jmeter GUI starts, in the console you will see the Jmeter version number that is being started.

## What is included here

In the ```src/test/jmeter``` folder you will find a number of sample Jmeter .jmx project files. After starting Jmeter, just browse to that folder and open one of the files with the Jmeter application.

*SauceLabs-Example.jmx* - An example of running Chrome browser tests from Jmeter within the SauceLabs cloud service.  Requires that you sign up to SauceLabs and create a free 2-thread account.    After signing up, get your ```sauce key```, open the ```SauceLabs-Example.jmx``` project file and then add your SauceLabs user key value in the included file called ```sauce-key.properties``` and put your SauceLabs username in the included file called ```sauce-user.properties``` .
