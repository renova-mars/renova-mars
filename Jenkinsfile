pipeline {
    options { 
        authorizationMatrix inheritanceStrategy: nonInheriting(), 
        permissions: [
                'GROUP:hudson.model.Item.Build:authenticated', 
                'USER:hudson.model.Item.Build:minh', 
                'USER:hudson.model.Item.Build:danghung', 
                'USER:hudson.model.Item.Cancel:minh', 
                'USER:hudson.model.Item.Cancel:danghung', 
                'USER:hudson.model.Item.Configure:minh', 
                'USER:hudson.model.Item.Configure:danghung', 
                'USER:hudson.model.Item.Delete:minh', 
                'USER:hudson.model.Item.Delete:danghung', 
                'GROUP:hudson.model.Item.Read:authenticated', 
                'USER:hudson.model.Item.Read:minh', 
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