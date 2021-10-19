pipeline {
    
    agent any

    stages {
        stage('Test') {
            steps {
              withCredentials([
                usernamePassword(credentialsId: 'testcreds', usernameVariable: 'USER', passwordVariable: 'PASS')
              ]) {
                script {
                    sh("print `echo $PASS | cut -c 0-9`")
                }
              }
            }
        }
    }
}
