pipeline {
    agent { label 'shopizer' } 
    triggers { cron(' * * * * *') }
        stages {
            stage('vcs'){
                steps {
                    git branch: 'develop', url: 'https://github.com/tejachennuru1/shopizer.git'
                }
            }
            stage('build'){
                steps {
                    sh 'mvn package'
                }
            }
            stage('archive results'){
                steps {
                    junit '**/target/surefire-reports/*.xml'
                }
            }
             stage('artifacts'){
                steps {
                    archiveArtifacts artifacts:  '**/target/*.jar'
                }
            }
        }
}

                  
    
    
        
       
    
