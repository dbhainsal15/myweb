node{
    stage('SCM Checkout'){
      git changelog: false, poll: false, url: 'https://github.com/javahometech/myweb'   
    }
  
    stage('Test'){
         sh "${mvnHome}/bin/mvn test"
    }
    stage('Package'){
         def mvnHome = tool name: 'maven', type: 'maven'
         sh "${mvnHome}/bin/mvn package"
    }
    
}
