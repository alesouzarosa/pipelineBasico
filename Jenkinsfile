pipeline { 
    agent any 

    options {
        skipStagesAfterUnstable()
    }
    triggers {
        pollSCM('H/2 * * * *')
    }
    stages {
        stage('Run Sh') { 
            steps {
                checkout scm
                sh 'env'
            }
        }
        stage('run aws cli'){
            steps {
                sh 'aws --version' 
            }
        }
        stage('De4ploy') {
            steps {
                sh 'echo fim'
            }
        }
    }
}