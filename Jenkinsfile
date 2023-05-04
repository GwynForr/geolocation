pipeline {
    agent any
    tools {
  maven 'M2_HOME'
}
    trigger {
  pollSCM '* * * * *'      
    }

    stages {
        stage('Build') {
            steps {
                sh 'mvn clean'
                sh 'mvn install'
                sh 'mvn package'
            }
        }
        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploy step '
            }
        }
        stage('Docker') {
            steps {
                echo 'Docker image'
            }
        }
    }
}
