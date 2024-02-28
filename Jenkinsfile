node{
 stage('git server'){
   echo "connecting to git server"
 }
 stage('fetching the cyberark provided credentials'){
   withCredentials([conjurSecretCredential(credentialsId: '329f72b5-30a1-473f-a572-82def713ab03', variable: 'CONJUR_SECRET')])
  {
        sh 'echo $CONJUR_SECRET |base64'
  }
 
  // git branch: 'main', credentialsId: 'new', url: 'https://github.com/ManithejaCyberark/conjur-quickstart.git'
  }
}
