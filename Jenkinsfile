pipeline {
    agent any

    stages {
        stage ("CheckoutCode") {
            steps {
                git branch: "master" , url: "https://github.com/Debi-Project/static-web-app.git"
            }
        }
        stage ("Deployment") {
            steps {
                sh 'scp -r /var/lib/jenkins/workspace/nginx Project ubuntu@ip-172-31-33-52/var/www/html
            }
        }
    }
}