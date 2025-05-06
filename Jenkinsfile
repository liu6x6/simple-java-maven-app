pipeline {
    agent any
    stages {
        stage('Build') { 
            steps {
                bat 'mvn -B -DskipTests clean package' 
            }
        }
        stage('test') {
            steps{
                bat 'mvn test'
            }
             post {
                always {
                    junit 'target/surefire-reports/*.xml' 
                }
            }
        }
    }
}