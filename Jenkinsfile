pipeline {
    agent any

    tools {
        maven 'maven3.9'
    }

    stages {
        stage ("CheckoutCode") {
            steps {
                git branch: 'master' , url: 'https://github.com/Debi-Project/My-Project.git'
            }
        }

        stage ("BuildCode") {
            steps {
                sh 'mvn clean package'
            }
        }
    }
}