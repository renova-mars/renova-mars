pipeline {
    options { authorizationMatrix(permissions('minh', ['hudson.model.Item.Create','hudson.model.Item.Discover'])) }
    agent none
    stages {        
        stage('base matrix test') {
            agent { node { label "jenkins-node-01" } }             
            steps {                
                script { 
                    properties([authorizationMatrix(
                        inheritanceStrategy: inheritingGlobal(), 
                        permissions: [
                            'hudson.model.Item.Build:minh', 
                            'hudson.model.Item.Cancel:minh',
                            'hudson.model.Item.Read:hoa',
                            'hudson.model.Item.Read:danghung'
                            ]
                        )]) 
                    sh "echo matrix works!!"                     
                }                
            }
        } 
    }    
}