pipeline {
    agent any
    stages {
        stage('Build') { 
            steps {
                cmd 'mvn -B -DskipTests clean package' 
            }
        }
    }
}