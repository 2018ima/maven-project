pipeline {
    agent any
    tools{
        maven 'local mvn'
    }
    
    stages{
        stage('Build'){
            steps {
                sh 'mvn clean package'
            }
            post {
                success {
                    echo 'save...'
                    archiveArtifacts artifacts: '**/target/*.war'
                }
            }
        }
    }
}
