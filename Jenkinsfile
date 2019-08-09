pipeline {
    agent any
    stages{
        stage('Build'){
            steps {
                sh 'mvn clean package'
            }
            post {
                success {
                    echo '我要存檔嚕...'
                    archiveArtifacts artifacts: '**/target/*.war'
                }
            }
        }
    }
}
