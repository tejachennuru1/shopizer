pipeline {
    agent{ label 'shopizer' } 
    triggers { pollSCM('* * * * *') }
        stages {
            stage('vcs'){
                steps{
                    git branch: devoper,
                        url   : 'https://github.com/tejachennuru1/devolp.git' 
                }
            }
            stage('build'){
                steps {
                    sh '/usr/bin/mvn package'
                }
            }
        }
}

                  
    
    
        
       
    
