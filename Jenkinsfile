pipeline{

agent any
     stages{
     stage('SCM code checkoout'){
     git'github.com/nagendra1037/nagendra1'
     }
        stage('compile stage'){
           steps{
            withMaven(maven :'maven3_5_0'){
               sh 'mvn clean compile'
               }
         }
      }
        stage('Testing stage'){
          steps{
            withMaven(maven :'maven3_5_0'){
               sh 'mvn test'
             } 
         }
      }
         stage('Deployement stage'){
           steps{
              withMaven(maven :'maven3_5_0'){
                sh 'mvn deploy'
             }
         }
      }
   }
}
