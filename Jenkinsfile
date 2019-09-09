pipeline {
    agent none 
    stages {
        stage('Build') { 
	    agent{lable 'lable1'}
            steps {
                checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/apurva1j/sample1.git']]])
            }
        }
        stage('Test') { 
	    agent{lable 'lable1'}
            steps {
                sh "echo Test"
            }
        }

        stage('Deploy') { 
	agent{lable 'lable1'}
            steps {
                bat "echo Deploy"
            }
        }
    }
}
