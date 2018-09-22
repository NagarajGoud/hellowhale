node{
    stage('Scm Checkout'){
    git credentialsId: 'git', url: 'https://github.com/NagarajGoud/hellowhale.git'
}

     stage('Build Docker'){
     sh 'docker build -t nagarajgoud/my-app:${BUILD_NUMBER} .'
}
 

   stage('Runcontainer on dev server'){

   sh 'docker run -p 8080:8080 -d --name my-kishan kishanpeddaboina/my-app:${BUILD_NUMBER}'
  
}

}