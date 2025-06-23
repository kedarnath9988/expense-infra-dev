pipeline {
    agent {
        label 'AGENT-01'
    }
    options {
        timeout(time: 30, unit: 'MINUTES')
        disableConcurrentBuilds()
        ansiColor('xterm')
    }
   

    stages {
        stage('init') {
            steps {
                sh """
                cd 01-vpc 
               ls -ltr 
                """
            }
        }
        stage('plan') {
            steps {
                 sh """
                echo 'this is plane;
                """
            }
        }
        stage('apply') {
            input {
                message "Should we continue?"
                ok "Yes, we should."
            }
            steps {
                 sh """
                echo 'this is apply'
                """
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


