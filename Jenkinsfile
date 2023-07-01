pipeline {
    agent any
    stages {
        stage('Build Application') {
            steps {
                echo "Now Archiving the Artifacts...."
                archiveArtifacts artifacts: '**/*.war'
            }
        }

        stage('Create Tomcat Docker Image'){
            steps {
                bat "pwd"
                bat "docker build . -t tomcatsamplewebapp:${env.BUILD_ID}"
            }
        }

    }
}