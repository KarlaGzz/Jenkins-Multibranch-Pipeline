pipeline {
    agent any
        stages {

            stage('First') {
                steps {
                    script{
                        env.VARIABLE = "True"
                        echo "Step One"
                    }
                    
                }
            }
 
            stage('Second') {
                steps {
                    when {
                        environment name: 'VARIABLE', value: 'True'
                        echo "${env.VARIABLE}"
                    }

                    script{
                        echo "Updating Second Stage"
                         
                    }
                   
                }
            } 

            stage('Third') {
                steps {
                   when {
                        environment name: 'VARIABLE', value: 'True'
                        
                    }
                    
                    script{
                        echo "Updating Thid Stage"
                         
                    }
                    echo "Step Three"
                }
            }
        }
}