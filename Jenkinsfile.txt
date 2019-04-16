node{
    stage('SCM Checkout'){
    git credentialsId: 'e25c0da9-0824-4738-b352-aaa231c9879c', url: 'https://github.com/vineether/maven-project.git'
    }
   stage('package'){
       def mvnHome = tool name: 'M2_HOME', type: 'maven'
        sh "${mvnHome}/bin/mvn clean package"
       
   }
   
}
