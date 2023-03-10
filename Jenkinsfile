node{
 stage('git server'){
   echo "connecting to git server"
 }
 stage('fetching the cyberark provided credentials'){
  withCredentials([conjurSecretUsername(credentialsId: 'from_jenkinsfile_github', passwordVariable: 'CONJUR_SECRET', usernameVariable: 'USERNAME')]) {
    echo "conjur provided credentials are : $CONJUR_SECRET and  $USERNAME"
    }
  // git branch: 'main', credentialsId: 'new', url: 'https://github.com/ManithejaCyberark/conjur-quickstart.git'
  }
}
