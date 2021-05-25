pipeline {
         agent any
         stages {
                stage('gitrepo') {
                steps {
                    sh '''#!/bin/bash
                    sudo yum update -y 
                    sudo yum install -y httpd
                    sudo systemctl start httpd
                    sudo systemctl enable httpd
                    mkdir site1
                    cd site1
                    git clone https://github.com/nilatac22/jenkins.git 
                    ls'''
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
