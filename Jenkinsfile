pipeline {
    agent any
        stages {

            stage('First') {
                steps {
                    script{
                        env.EXECUTE = "True"
                        sh ' echo "Step One" '
                    }
                    
                }
            }
 
            stage('Second') {
                steps {
                    when {
                        environment name: 'EXECUTE', value: "True"
                        
                    }

                    script{
                        sh ' echo "Updating Second Stage" '
                         
                    }
                   
                }
            } 

            stage('Third') {
                steps {
                   when {
                        environment name: 'EXECUTE', value: "True"
                        
                    }
                    
                    script{
                        sh ' echo "Updating Thid Stage" '
                         
                    }
                   
                }
            }
        }
}