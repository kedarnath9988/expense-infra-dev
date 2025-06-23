pipeline {
    agent {
        label 'AGENT-01'
    }
    options {
        timeout(time: 30, unit: 'MINUTES')
        disableConcurrentBuilds()
    }
   

    stages {
        stage('init') {
            steps {
                sh """
                    echo 'this is init stage'
                """
            }
        }
        stage('plan') {
            steps {
                 sh 'echo this Test stage '
            }
        }
        stage('apply') {
            steps {
                 sh 'echo this Deploy stage............... '
            }
        }
    }
    post { 
        always { 
            echo 'I will always say Hello again!'
            deleteDir()
        }
        success {
            echo 'I pipeline is always success'
        }
        failure {
            echo ' Hi pipeline failure '
        }
    }
    }


