# php-jenkins

Following installation/setup is w.r.t. Linux.
Please, do commit the repository docs, build.xml, phpmd.xml, etc., if required.

## Required PHP tools
Install following tools w.r.t. to your PHP version:
* PHPUnit

        $ cd
        $ wget -O phpunit https://phar.phpunit.de/phpunit-4.phar
        $ chmod +x phpunit
        $ sudo mv phpunit /usr/local/bin/

* PHP_CodeSniffer

        $ cd
        $ wget -O https://squizlabs.github.io/PHP_CodeSniffer/phpcs.phar
        $ chmod +x phpcs
        $ sudo mv phpcs /usr/local/bin/

* PHPLOC

        $ cd
        $ wget -O phploc https://phar.phpunit.de/phploc.phar
        $ chmod +x phploc
        $ sudo mv phploc /usr/local/bin/

* PHP_Depend

        $ cd
        $ wget -O pdepend http://static.pdepend.org/php/latest/pdepend.phar
        $ chmod +x pdepend
        $ sudo mv pdepend /usr/local/bin/
                                                                                                   
* PHPMD                                                                                            
        $ cd                                                                                       
        $ wget -O phpmd http://static.phpmd.org/php/latest/phpmd.phar                              
        $ chmod +x phpmd                                                                           
        $ sudo mv phpmd /usr/local/bin/                                                            
                                                                                                   
* PHPCPD                                                                                           

        $ cd                                                                                       
        $ wget -O phpcpd https://phar.phpunit.de/phpcpd.phar                                       
        $ chmod +x phpcpd                                                                          
        $ sudo mv phpcpd /usr/local/bin/                                                           
                                                                                                   
* phpDox                                                                                           

        $ cd                                                                                       
        $ wget -O phpdox http://phpdox.de/releases/phpdox.phar                                     
        $ chmod +x phpdox                                                                          
        $ sudo mv phpdox /usr/local/bin                                                            
                                                                                                   
## Jenkins Installation                                                                            
Follow the steps [here](https://jenkins.io/doc/book/installing/#linux) to install jenkins.         
                                                                                                   
## Jenkins Setup                                                                                   
                                                                                                   
> Jenkins Post Installation:                                                                       
                                                                                                   
* Create host entry in windows.                                                                    
* Go to http://jenkins-name-in-host-file:8080, e.g. jenkins.lh                                     
* To set admin password, go to vagrant box and do                                                  
                                                                                                   
        $ cat /var/lib/jenkins/secrets/initialAdminPassword                                        
* Copy the hash and paste in the "Getting Started" dialog.                                         
                                                                                                   
> Install Jenkins Plugins:
<br>It installs the required plugins during first setup.
<br>In case required plugins are missed, do it manually mentioned in below list.
* Login to Jenkins Web App
* Go to "Manage Jenkins" -> "Manage Plugins"
* Select "Available" tab
* Search and select following plugins:
    * Ant
    * Credentials
    * Checkstyle
    * Crap4j
    * Clover PHP
    * DRY
    * HTML Publisher
    * JDepend
    * PMD
    * Plot
    * Subversion
    * Violations
    * Warnings
    * xUnit
* Click "Install without restart"

## Create your project  pipeline
* Click **New item**
* Add name for your project
* Add svn repository link and credentials
* Click **Build Now**

## Clone/download php-jenkins
* Clone/download php-jenkins build file(s) [here](https://github.com/DXBlr/php-jenkins.git).
* Copy files and directories to your repository.
* Change the build.xml and other builds in build(directory) w.r.t. your project, if required.

