pipeline {
    agent {
        docker {
            image 'node:lts-buster-slim' 
            args '-p 3000:3000' 
        }
    }
    environment {
        CI = 'true'
    }
    stages {
//         stage('Build') { 
//             steps {
//                 sh 'npm install' 
//             }
//         }
//         stage('Test') {
//             steps {
//                 sh './jenkins/scripts/test.sh'
//             }            
//         }
        stage('Deliver') {
            steps {
                sh 'pwd'
                sh 'ls -l /'
                sh 'ls -l /home/'
                sh 'ls -l /var/'
//                 sh 'ls -l /var/jenkins_home/'
//                 sh './jenkins/scripts/deliver.sh'
//                 sh 'cp ./jenkins/scripts/*.sh /home/www/'
//                 input message: 'Finished using the web site? (Click "Proceed" to continue)'
//                 sh './jenkins/scripts/kill.sh'
            }
        }
    }
    post {
        always {
            sh 'pwd'
            sh 'ls -l /'
            sh 'ls -l /home/'
            sh 'ls -l /var/'
//             sh 'ls -l /var/jenkins_home/'
            sh 'ls -l ./'
        }
    }
}
