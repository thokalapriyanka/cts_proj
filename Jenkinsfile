pipeline {
 agent any
  stages {
      stage('Pull') {
         steps {
             git 'https://github.com/thokalapriyanka/cts_proj.git'
         }
      }
     /* stage('Compile') {
         steps {
            bat 'mvn compile'
         }
      }
	   stage('Test') {
         steps {
            bat 'mvn test'
         }
      }*/
	   stage('Package') {
         steps {
            bat 'mvn package'
         }
      }
      stage('Execute') {
         steps {
            bat 'java -jar "C:/Windows/System32/config/systemprofile/AppData/Local/Jenkins/.jenkins/workspace/projcts_pipeline/target/projcts-1.0-SNAPSHOT.jar"'
         }
      }
   }
}
