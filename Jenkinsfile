pipeline {
    agent any
    stages {
        stage('Build Application') {
            steps {
                sh 'mvn -f my-app/pom.xml clean package'
            }
            post {
                success{
                    echo "Now Archiving the Artifacts ..."
                    echo "==============================="
                    archiveArtifacts artifacts: '**/*.jar'
                    echo "==============================="
                }
            }
        }
    }
}