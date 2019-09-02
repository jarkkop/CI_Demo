node{
  stage('SCM Checkout'){
    git 'https://github.com/jarkkop/CI_Demo'
  }
  stage('Compile-Package'){
    bat 'mvn package'
  }

}
