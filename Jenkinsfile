pipeline {
    agent { label 'shopizer' } 
    triggers { pollSCM('30 5 * * * *') }
        stages {
            stage('vcs'){
                steps {
                    git branch: develop,
                        url   : 'https://github.com/tejachennuru1/shopizer.git' 
                }
            }
            stage('build'){
                steps {
                    sh 'mvn package'
                }
            }
        }
}

                  
    
    
        
       
    
