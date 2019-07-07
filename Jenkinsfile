pipeline {
   agent any

   stages {

       stage ('SCM Checkout') {

           steps {
             git 'https://github.com/anita0316/maven-project'
               }
           }

       stage ('Compile Stage') {

           steps {
               withMaven(maven : 'maven') {
                   sh 'mvn compile clean'

               }
           }
       }

       stage ('Testing Stage') {

           steps {
               withMaven(maven : 'maven') {
                   sh 'mvn test'
               }
           }
       }

       stage ('Package Stage') {
           steps {
               withMaven(maven : 'maven') {
                   sh 'mvn package'
               }
           }
       }

       stage ('verify Stage') {
           steps {
               withMaven(maven : 'maven') {
                   sh 'mvn verify'
               }
           }
       }
   }
}
