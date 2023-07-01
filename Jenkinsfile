pipeline{
    agent any
    stages {
        stage('Archive the artifacts'){
            steps{
                    echo "Archiving the Artifacts..."
                    archiveArtifacts artifacts: '**/*.war'
                }
            }
        }
        stage('Create Tomcat Docker Image'){
            steps{
                sh 'docker build . -t tomcatsamplewebapp:${env.BUILD_ID}'
            }
        }
    }
