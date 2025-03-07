pipeline{
    
    agent any
    stages{
        stage("Dev-Team-credentials"){
            steps{
                 withCredentials([conjurSecretCredential(credentialsId: 'conjur_provided_dev-team-1cred', variable: 'CONJUR_SECRET_DEV_TEAM')])  {
                  sh 'echo $CONJUR_SECRET_DEV_TEAM | base64'
                }
            }
        }
        stage("test-pipeline Credentials"){
             steps {
                script {
                    userVar = null
                    passVar = null
                    withCredentials([usernamePassword(credentialsId: 'jenkins_cred', passwordVariable: 'testPwd', usernameVariable: 'testUserName')]) {
                        userVar = testUserName
                        passVar = testPwd
                    }
                    echo "Username: ${userVar}"
                    echo "Password: ${passVar}"
                }
            }
        }
    }
}
