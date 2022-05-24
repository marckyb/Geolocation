pipeline {
    triggers {
  pollSCM '* * * * *'
}
   agent any
   tools {
  maven 'M2_HOME'
}
    
    stages {
        stage('maven package') {
            steps {
               sh 'mvm clean'
               sh 'mvn install'
               sh 'mvm package'
            }
        }
            stage('test') {
            steps {
                sh 'mvn test'
                
            }
        }
            
            stage('Deploy') {
            steps {
                echo 'Deploy'
            }
       
        }
    }
}