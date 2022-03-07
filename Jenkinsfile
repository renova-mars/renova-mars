pipeline { 
     agent none 
     stages { 
          stage('base matrix test') { 
              agent { node { label "jenkins-worker-ng" } } 
              steps { 
                  script { 
                     properties([authorizationMatrix(['hudson.model.Item.Build:Pupkin'])]) 
                     sh "echo matrix works!!" 
                  } 
              } 
          }  
      } 
}