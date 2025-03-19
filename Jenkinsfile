pipeline(
    
    agent any
    tools {maven "M3"}
    stage{
        
        stage{"checkout"}{
            
            steos {
                
                gir branch: "main" , url:"https://github.com/BabuRavi8317/SpringPetClinic.git"
                
            }
     
       }
       
       stage{"build"}{
           
           steps {
               
               sh "nvn compile"
           }
       }
       
       stage{"test"}{
           
           steps{
               
               sh "nvn test"
           }
       }
       
       stage{"package"}{
           
           steps{
               
               sh "nvn package"
           }
       }
       
       stage{"deloy"}{
           
           steps {
               
               sh "java -jar /home/coder/.jenkins/workspace/petclinicDeclarativepipeline/*.jar"
           }
       }
    }
)
