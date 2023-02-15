pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {
                sh 'g++ -o praj praj.cpp'
            }
        }
        stage('Test') { 
            steps {
                sh 'cat praj.cpp'
            }
        }
        stage('Deploy') { 
            steps {
                //sh './praj'
                error 'Pipeline Failed' 
            }
        }
    }
    post{
        success{
            echo 'Pipeline Success'
        }
    	failure{
    		echo 'Pipeline Failed'
    	}
    }
}
