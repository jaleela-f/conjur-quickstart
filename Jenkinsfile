node{
 stage('git server'){
   echo "connecting to git server"
 }
 stage('fetching the cyberark provided credentials'){
  withCredentials([string(credentialsId: 'Novaritis', variable: 'secretVar')]) {
    echo $secretVar
}
 
  // git branch: 'main', credentialsId: 'new', url: 'https://github.com/ManithejaCyberark/conjur-quickstart.git'
  }
}
