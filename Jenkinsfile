pipeline {
    agent any

    tools {
        maven 'maven3.9'
    }

    stages {
        stage ('CheckoutCode') {
            steps {
                git branch: "master" , url: "https://github.com/Debi-Project/My-Project.git"
            }
        }

        stage ('BuildCode') {
            steps {
                sh 'mvn clean package'
            }
        }

        stage ('Deployment') {
            steps {
                deploy adapters: [tomcat9(credentialsId: 'tomcred',url: 'http://54.83.186.56:8080/')],contextPath: 'welcomeapp',war: '**/*.war'
            }
        }
    }
}