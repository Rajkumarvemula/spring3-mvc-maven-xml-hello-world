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
      sh "'${mvnHome}/bin/mvn' clean package"
      } 
   stage ('deploy'){
   echo 'deployment started'
       bat '''copy C:\\Users\\Madhu\\.jenkins\\workspace\\jmsth20-pipeline-tomcat\\target\\*.war F:\\softwares\\apache-tomcat-7.0.53\\webapps\\'''
   }  
   
}
