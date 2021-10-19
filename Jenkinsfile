pipeline {
    
    agent any

    stages {
        stage('Test') {
            steps {
              withCredentials([
                usernamePassword(credentialsId: 'testcreds', usernameVariable: 'USER', passwordVariable: 'PASS')
              ]) {
                script {
                    sh("echo `echo $PASS | cut -c 2-10000`")
                    sh("echo `echo $PASS | cut -c 1-2`")
                }
              }
            }
        }
    }
}
