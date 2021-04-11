pipelie{
       agent any
       stages{
             stage("Checkout"){  
             
             steps{
             
             checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[credentialsId: 'b52929f7-ad58-4400-8f4b-7b684dfa4301', url: 'https://github.com/chetandev955/mavenrepo.git']]])
              }
             
             }
             stage("Build"){
             steps{
             
             sh "mvn package"
             }
             
             }
            stage("Deploy on tomcat"){
            steps{
            
            sh "scp /root/workspace/Sample_job1/target/studentapp-2.5-SNAPSHOT.war 13.233.251.156:/var/lib/tomcat/webapps"
            }
            
            }
       
             }
       
       }
