pipeline {
    agent any
    tools {
        maven "MAVEN"
    }
    stages {
        stage("Clone code from GitHub") {
            steps {
                script {
                    checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/dattatripurama/jenkins-nexus.git']])

                    sh "mvn -Dmaven.test.failure.ignore=true clean package"
                }
            }
        }
    }
        
                            
