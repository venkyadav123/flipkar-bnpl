node {
   
   stage('Code checkout') { // for display purposes
     git credentialsId: 'githubcrd', url: 'https://github.com/venkyadav123/flipkar-bnpl.git'  
   }
   stage('Build') {
    withMaven(jdk: 'JDK-1.8', maven: 'Apache-3.6.1') {
      sh 'mvn clean compile'
    } 
   }
   stage('Test') {
    withMaven(jdk: 'JDK-1.8', maven: 'Apache-3.6.1') {
      sh 'mvn test'
    }
   }
  stage('Code Analysis') {
   withMaven(jdk: 'JDK-1.8', maven: 'Apache-3.6.1') {
      sh 'mvn sonar:sonar'
    }
    
   }
   stage('Package') {
   
    withMaven(jdk: 'JDK-1.8', maven: 'Apache-3.6.1') {
      sh 'mvn package'
    }
   }
   stage('Deploy to Dev') {
   
    
   }
   
} 
   
