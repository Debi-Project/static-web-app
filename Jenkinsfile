pipeline {
    agent any
    tools {
        mvn 'maven3.9'
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
    }
}