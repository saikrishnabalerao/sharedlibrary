
pipeline {
    agent any
    
    tools{
        maven "Maven-3.9.4"
    }

    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/saikrishnabalerao/sharedlibrary.git'
            }
        }
         stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }
    }
}
