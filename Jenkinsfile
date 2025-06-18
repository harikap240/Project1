pipeline {  
      agent { label 'Jenkins-agent' }
      tools {
          jdk 'Java17'
          maven 'Maven3'
      }
      stages{
          stage("cleanup work space"){
            steps  {
              cleanWs()
            }
          }

        
        stage('Checkout Code') {
            steps {
                git branch:  'main' , credentialsId: 'github', url: 'https://github.com/harikap240/Project1'
            }

          
      }
}
