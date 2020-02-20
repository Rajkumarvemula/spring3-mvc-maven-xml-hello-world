node {
   def mvnHome
   stage('getscm') { // for display purposes
      // Get some code from a GitHub repository
      git 'https://github.com/ybmadhu/spring3-mvc-maven-xml-hello-world.git'
      // Get the Maven tool.
      // ** NOTE: This 'M3' Maven tool must be configured
      // **       in the global configuration.           
       mvnHome = tool 'Maven'
     
   }
   stage('Build') {
      // Run the maven buil
      sh "mvn clean package"
      } 
   stage ('copy war file to ansible server'){
   echo 'copying started'
     
       sh "cp /var/lib/jenkins/workspace/EXAM-PIPELINE/target/*.war /home/jenkins"
   }  
   
}
