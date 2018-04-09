# php-jenkins

Following installation/setup is w.r.t. Linux.
Please, do commit the repository docs, build.xml, phpmd.xml, etc., if required.

## Installation
Follow the steps [here](https://jenkins.io/doc/book/installing/#linux) to install jenkins.

## Setup

> Jenkins Post Installation:

* Create host entry in windows.
* Go to http://jenkins-name-in-host-file:8080, e.g. jenkins.lh
* To set admin password, go to vagrant box and do

        $ cat /var/lib/jenkins/secrets/initialAdminPassword
* Copy the hash and paste in the "Getting Started" dialog.

> Install Jenkins Plugins:
It installs the required plugins during first setup.
In case if it missed some, do it manually.
* Login to Jenkins Web App
* Go to "Manage Jenkins" -> "Manage Plugins"
* Select "Available" tab
* Search and select following plugins:
    * Subversion Plugin
    * Checkstyle Plugin
    * Git Plugin
    * PMD Plugin
    * HTML Publisher Plugin
    * Plot Plugin
    * xUnit
    * Ant Plugin  
    * Static Analysis Utitlities  
    * Credentials Plugin  
    * Duplicate Code Scanner Plug-in  
    * Jenkins JDepend Plugin  
    * Plot plugin  
* Click "Install without restart"

## Create your project  pipeline
* Click **New item**
* Add name for your project
* Add svn repository link and credentials
* Click **Build Now**

## Clone/download php-jenkins
* Clone/download php-jenkins build file(s) [here]().
* Copy files and directories to your repository.
* Change the build.xml w.r.t. your project, if required.
 
## Reconfigure your project 
* Select your project
* Click **Configure**
* Add post-build action(s), like phpmd, phpcs, etc
* Click **Save**
* Click **Build Now**


