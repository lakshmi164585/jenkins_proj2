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
                git branch 'main' , credentialsId: 'github' , url: ''
              }
         stage ("Build application") {
              steps {
                cleanws {
                    
                }
              }
          }
     }
}