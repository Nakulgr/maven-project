pipeline {
    agent any
    stages{
        stage('Build'){
            steps {
                C:\Program Files\Git\bin\sh.exe 'mvn clean package'
            }
            post {
                success {
                    echo 'Now Archiving...'
                    archiveArtifacts artifacts: '**/target/*.war'
                }
            }
        }
    }
}