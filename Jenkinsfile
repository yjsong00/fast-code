pipeline {
    agent any
    environment {
        GITNAME = "yjsong00"
        GITMAIL = "yjsong0088@gmail.com"
        GITWEBADD = "https://github.com/yjsong00/fast-code.git"
        GITSSHADD = "git@github.com:yjsong00/fast-code.git"
        GITCREDENTIAL = "git_cre"
        DOCKERHUB = 'reneeins/fast'
        DOCKERHUBCREDENTIAL = 'docker_cre'
    }
    stages {
        stage('Checkout Github') {
            steps {
                checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [],
                userRemoteConfigs: [[credentialsId: GITCREDENTIAL, url: GITWEBADD]]])

            }
            post {
                failure {
                    sh "echo failed"
                }
                success {
                    sh "echo success"
                }
            }
        }
        stage('start') {
            steps {
                sh "echo hello jenkins!!!"
            }
            post {
                failure {
                    sh "echo failed"
                }
                success {
                    sh "echo success"
                }
            }
        }

    }
}
