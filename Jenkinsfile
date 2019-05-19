node{
    stage('SCM Checkout'){
      git changelog: false, poll: false, url: 'https://github.com/dbhainsal15/myweb'   
    }
  
    stage('Test'){
         sh "${mvnHome}/bin/mvn test"
    }
    stage('Package'){
         def mvnHome = tool name: 'maven-3', type: 'maven'
         sh "${mvnHome}/bin/mvn package"
    }
    
}
