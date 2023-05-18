node{
 stage('git server'){
   echo "connecting to git server"
 }
 stage('fetching the cyberark provided credentials'){
  withCredentials([conjurSecretCredential(credentialsId: 'conjur_secrets_from_pipeline_gihub_login', variable: 'CONJUR_SECRET')]) {
        sh "echo $CONJUR_SECRET | base64"
    }
  // git branch: 'main', credentialsId: 'new', url: 'https://github.com/ManithejaCyberark/conjur-quickstart.git'
  }
}
