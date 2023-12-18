pipeline {
    agent any
    tools {
        maven 'maven3.9'
    }
    stages {
        stage ("CheckoutCode") {
            steps {
                git branch: "master" , url: "https://github.com/Debi-Project/My-Project.git"
            }
        }
        stage ("DeployCode") {
            steps {
                sh 'mvn clean package'
                echo "DeployCode successed"
            }
        }

        stage ("Deployment") {
            steps {
                deploy adapters: [tomcat9 (credentialsId: "tomcred",url: "http://34.224.65.98:8080/")], contextPath: "welcomeapp", war: "**/*.war"
            }
        }
    }
}