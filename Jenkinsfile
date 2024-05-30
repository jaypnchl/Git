pipeline {
    agent any
    stages {
        stage('Make executable') {
            steps {
                sh('chmod +x ./fibonacci.sh')
            }
        }
        stage('Relative path') {
            steps {
                sh("./fibonacci.sh 10")
            }
        }
        stage('Full path') {
            steps {
                sh("${env.WORKSPACE}/fibonacci.sh 10")
            }
        }
        stage('Change directory') {
            steps {
                dir("${env.WORKSPACE}"){
                    sh("./fibonacci.sh 10")
                }
            }
        }
    }
}
