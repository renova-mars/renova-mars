pipeline {
    //options { authorizationMatrix(permissions('minh', ['hudson.model.Item.Create','hudson.model.Item.Discover'])) }
    agent none
    stages {        
        stage('matrix test') {
            agent { node { label "jenkins-node-01" } }             
            steps {                
                script { 
                    properties([authorizationMatrix(
                        inheritanceStrategy: inheritingGlobal(), 
                        permissions: [
                            'hudson.model.Item.Create:minh',
                            'hudson.model.Item.Discover:minh',
                            'hudson.model.Item.Build:minh', 
                            'hudson.model.Item.Cancel:minh',
                            'hudson.model.Item.Discover:hoa',
                            'hudson.model.Item.Read:hoa',
                            'hudson.model.Item.Discover:danghung',
                            'hudson.model.Item.Read:danghung'
                            ]
                        )]) 
                    sh "echo matrix works!!"                     
                }
            }
        }
        stage('build') {
            agent { docker { image 'python:3.10.1-alpine' } }
            steps {
                sh 'python --version'
            }
        } 
    }
    post { 
        success { 
            echo 'Fin'
        }
    }    
}