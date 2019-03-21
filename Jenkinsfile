pipeline {
    agent any
        stages {

            stage('First') {
                steps {
                    script{
                        env.EXECUTE = "False"
                        echo "First Step" 
                    }
                }
            }
 
            stage('Second') {
                    when {
                        environment name: 'EXECUTE', value: "True"
                    }   
                    steps{
                        echo "Updating Second Stage"     
                    }
           } 

            stage('Third') {
                when {
                        environment name: 'EXECUTE', value: "True"
                        
                }
                
                steps {
                     echo "Updating Third Stage" 
                }
            }
        }
}