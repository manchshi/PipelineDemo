node{
      def mvnHome = tool name: 'Maven 3.6.1', type: 'maven' 
      stage('Checkout'){
         git 'https://https://github.com/manchshi/PipelineDemo'
       
      }  
      stage('Build'){
         //// Get maven home path and build
        sh "${mvnHome}/bin/mvn clean package -Dmaven.test.skip=true"
      }
     stage ('Test-JUnit'){
         sh "'${mvnHome}/bin/mvn' test surefire-report:report"
      }  
                            
                   
     }
      
 }
