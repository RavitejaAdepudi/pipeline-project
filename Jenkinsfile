pipeline {
    agent any

    stages {
        stage ('Compile Stage') {

            steps {
                withMaven(maven : 'maven_3_5_0') {
                    sh 'mvn clean install'
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
             
       
                  
                  sh 'cp root@ip-172-31-21-9:./target/*.war /opt/apache-tomcat-8.5.29/webapps/'
                  
                  }
                  
                  }
        

 
        
    }
}
