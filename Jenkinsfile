pipeline {
    agent any
    environment {
        PATH = "/opt/apache-maven-3.6.3/bin:$PATH"
    }
    stages {
        stage('clone code') {
            steps {
                git 'https://github.com/CICD-jalaj/Pipeline_Job.git'
            }
        }
         stage('build code') {
            steps {
                sh "mvn clean install"
            }
        }
         stage('Test code') {
            steps {
                sh "mvn test"
            }
        }
       
    }
}
