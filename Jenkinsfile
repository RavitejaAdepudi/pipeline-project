pipeline {
    agent any

    stages {
        stage ('Compile Stage') {

            steps {
                withMaven(maven : 'maven_3_5_0') {
                    sh 'mvn clean compile'
                }
            }
        }

        stage ('Testing Stage') {

            steps {
                withMaven(maven : 'maven_3_5_0') {
                    sh 'mvn test'
                }
            }
        }
        stage('Deploy to Tomcat'){
            steps {
            
       
                  
                  sh 'scp -o StrictHostKeyChecking=no target/*war http://13.127.248.227:/opt/apache-tomcat-8.5.29/webapps/'
                  
                  }
                  
                  }
        

 
        
    }
}
