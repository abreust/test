pipeline {
    
    agent any

    stages {
        stage('Test') {
            steps {
              withCredentials([
                usernamePassword(credentialsId: 'testcreds', usernameVariable: 'USER', passwordVariable: 'PASS')
              ]) {
                script {
                    sh("USER=hi;echo ${PASS}" && echo $USER:$PASS")
                }
              }
            }
        }
    }
}
