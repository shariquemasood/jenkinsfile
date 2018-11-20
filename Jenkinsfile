pipeline {
    agent any
    stages {
        stage('Getting Git Pull') {
            steps {
                echo 'Preparation..'
                // Get some code from a GitHub repository
                git 'https://github.com/Silverpop/sample-helloworld-ant.git'
            }
        }
        stage('Build') {
            steps {
                echo 'Building..'
                 withAnt(installation: 'ant', jdk: 'java') {
                  sh 'ant'
                }
            }
        }
    }
}
