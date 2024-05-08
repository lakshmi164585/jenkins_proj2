pipeline {
    agent { label 'latestnode'}
    tools {
        jdk 'java17'
        maven 'maven3'
    }
     stages{
          stage ("cleanup workspace") {
              steps {
                cleanws {

                }
              }
          stage ("chekout from SCM") {
              steps {
                  git branch 'main' , credentialsId: 'github' , url: 'https://github.com/lakshmi164585/jenkins_proj2'
              }
          }
         stage ("Build application") {
              steps {
                sh "mvn clean package " 
                    
                }
              }
          }
     }
         stage ("Test application") {
              steps {
                sh "mvn test"   

}
     }
}
}
