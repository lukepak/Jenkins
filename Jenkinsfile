peline { 
    agent any 
    
    stages {
        stage('Complile Stage') { 
            steps { 
                withMave(maven : 'maven_3_6_3') {
                sh 'mvn clean copile'
               } 
            }
        }
        stage('Testing Stage'){
            steps {
                withMaven(maven : 'maven_3_6_3') {
                 sh 'mvn test'
                }
            }
        }
        stage('Deploy') {
            steps {
               withMaven(maven : 'maven_3_6_3') {
                 sh 'mvn deploy'
               }
            }
        }
    }
}
