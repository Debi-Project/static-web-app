pipeline {
    agent any

    stages {
        stage ("CheckoutCode") {
            steps {
                git branch: "master" , url: "https://github.com/Debi-Project/static-web-app.git"
            }
        }
    }
}