pipeline {
         agent any
         stages {
                stage('git repo') {
                steps {
                    sh '''#!/bin/bash
                    sudo yum update -y 
                    sudo yum install -y httpd
                    sudo systemctl start httpd
                    sudo systemctl enable httpd
                    mkdir site 
                    cd site
                    git clone https://github.com/nilatac22/jenkins.git 
                    ls
                    cp index.html /var/www/html/
                    sudo chmod 766 /var/www/html/index.html'''
                 }
                }
                 stage('Test') {
                 steps {
                    echo 'Httpd was installed'
                 }
                 }
              stage('End') {
      steps {
        echo 'End of pipeline'
      }
    }
         }
}
