pipeline {

    stages {
        stage('Test') {
            steps {
              withCredentials([
                usernamePassword(credentialsId: 'testcreds', usernameVariable: 'USER', passwordVariable: 'PASS')
              ]) {
                script {
                  sh("echo $USER:$PASS")
                }
              }
            }
        }
    }
}
