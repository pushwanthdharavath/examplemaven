pipeline {
    agent any

    tools {
        maven 'maven3'
    }

    environment {
        PATH = "C:\\Program Files\\maven\\bin;${env.PATH}"
    }

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/pushwanthdharavath/examplemaven.git'
            }
        }

        stage('Build') {
            steps {
                bat '"C:\\Program Files\\maven\\bin\\mvn" clean install'
            }
        }
    }
}
