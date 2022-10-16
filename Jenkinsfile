pipeline {
    agent { label 'shopizer' } 
    triggers { pollSCM('*/2 * * * *') }
        stages {
            stage('vcs'){
                steps {
                    git branch: devoper,
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

                  
    
    
        
       
    
