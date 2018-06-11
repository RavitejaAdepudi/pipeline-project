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
             
       
                  
                  sh 'scp root@ip-172-31-21-9:./target/*.war root@ip-172-31-21-9:/opt/apache-tomcat-8.5.29/webapps/'
                  
                  }
                  
                  }
        

 
        
    }
}
