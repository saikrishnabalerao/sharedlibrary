@Library('ashokit_shared_lib') _

pipeline {
    agent any    
    tools{
        maven "Maven-3.9.4"
    }
    stages {
        stage('Clone') {
            steps {
             git branch: 'main', credentialsId: 'GIT-CREDENTIALS', url: 'https://github.com/saikrishnabalerao/sharedlibrary.git'
            }
        }
        stage('Maven Build'){
            steps{
              mavenBuild()
            }
        }
		stage('Code Review'){
			steps{
				sonarQube()
			}
		}
    }
}
