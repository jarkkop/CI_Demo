node{
  stage('SCM Checkout'){
    git 'https://github.com/jarkkop/CI_Demo'
  }
  stage('Compile-Package'){
    //Get maven home path
    def mvnHome = tool name: 'Maven_3.6.0', type: 'maven'
    sh "${mvnHome}/bin/mvn package"
//    bat 'mvn package'
  }

}
