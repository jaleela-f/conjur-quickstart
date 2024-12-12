pipeline {
    agent any
 
    stages {
        stage('Folder-1-Conur-Credentials') {
            steps {
                script{
                    varVal =null
                withCredentials([conjurSecretCredential(credentialsId: 'jaleela-f', variable: 'CONJUR_SECRET')]) {
                        varVal = CONJUR_SECRET
                    }
                echo "Folder-1-Conjur Cred Val  : ${varVal}"
                }
            }
        }
 
}
