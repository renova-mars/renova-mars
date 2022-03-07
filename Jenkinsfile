pipeline {
    options { 
        authorizationMatrix inheritanceStrategy: nonInheriting(), 
        permissions: [ 
                'USER:hudson.model.Item.Build:danghung', 
                'USER:hudson.model.Item.Cancel:danghung', 
                'USER:hudson.model.Item.Configure:danghung', 
                'USER:hudson.model.Item.Delete:danghung', 
                'GROUP:hudson.model.Item.Read:authenticated', 
                'USER:hudson.model.Item.Read:danghung'
            ] 
        }
    agent none
    stages {        
        stage('matrix test') {
            steps {                
                sleep 10
                echo 'Hello World'
            }
        }
    }
    post { 
        success { 
            echo 'Fin'
        }
    }    
}