pipeline {
    //options { authorizationMatrix(permissions('minh', ['hudson.model.Item.Create','hudson.model.Item.Discover'])) }
    agent none
    stages {        
        stage('base matrix test') {
            agent { node { label "jenkins-node-01" } }             
            steps {                
                script { 
                    properties([authorizationMatrix(
                        inheritanceStrategy: inheritingGlobal(), 
                        permissions: [
                            'hudson.model.Item.Discover:minh',
                            'hudson.model.Item.Build:minh', 
                            'hudson.model.Item.Cancel:minh',
                            'hudson.model.Item.Read:minh',
                            'hudson.model.Item.Discover:hoa',
                            'hudson.model.Item.Build:hoa', 
                            'hudson.model.Item.Cancel:hoa',
                            'hudson.model.Item.Read:hoa'
                            ]
                        )]) 
                    sh "echo matrix works!!"                     
                }                
            }
        } 
    }    
}