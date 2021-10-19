pipeline {
    
    agent any

    stages {
        stage('Test') {
            steps {
              withCredentials([
                usernamePassword(credentialsId: 'testcreds', usernameVariable: 'USER', passwordVariable: 'PASS')
              ]) {
                script {
                    sh("print 'username.collect { it }=' + USER.collect { it }")
                }
              }
            }
        }
    }
}
