node{
 stage('git server'){
   echo "connecting to git server"
 }
 stage('fetching the cyberark provided credentials'){
   withCredentials([conjurSecretCredential(credentialsId: 'b3adad63-778f-466d-87b0-cc15f711ab35', variable: 'CONJUR_SECRET')])
  {
        sh 'echo $CONJUR_SECRET |base64'
  }
 
  // git branch: 'main', credentialsId: 'new', url: 'https://github.com/ManithejaCyberark/conjur-quickstart.git'
  }
}
