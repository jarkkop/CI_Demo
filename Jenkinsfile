node{
  stage('SCM Checkout'){
    git 'https://github.com/jarkkop/CI_Demo'
  }
  stage('Compile-Package'){
    //Get maven home path
    def mvnHome = tool name: 'Maven_3.6.0', type: 'maven'
    bat "${mvnHome}/bin/mvn package"     //Windows
//    sh "${mvnHome}/bin/mvn package"    //Linux
//    bat 'mvn package'                 //Windows
  }

}
