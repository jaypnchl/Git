pipeline {
    agent any
    stages {
        stage('Make executable') {
            steps {
                sh('chmod +x ./scripts/fibonacci.sh')
            }
        }
        stage('Relative path') {
            steps {
                sh("./scripts/fibonacci.sh 10")
            }
        }
        stage('Full path') {
            steps {
                sh("${env.WORKSPACE}/scripts/fibonacci.sh 10")
            }
        }
        stage('Change directory') {
            steps {
                dir("${env.WORKSPACE}/scripts"){
                    sh("./fibonacci.sh 10")
                }
            }
        }
    }
}
