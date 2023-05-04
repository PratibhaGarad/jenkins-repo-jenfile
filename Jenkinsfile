pipeline {
    agent {
        label {
            label "node-1"
            customWorkspace "/mnt/customnode-space"
        }
    }

    stages {
        stage ('Compile Stage') {

            steps {
                    sh 'sudo rm -rf /root/.m2/repository'
                    sh 'sudo mvn clean compile'
                }
            
        }

        stage ('Testing Stage') {

            steps {
                
                    sh 'mvn test'
                }
            
        }


        stage ('Install Stage') {
            steps {
                
                    sh 'mvn install'
                }
            
        }
        
        stage ('Echo Branch') {

            steps {
                
                    echo "This is dev branch"
                }
            
        }
    }
}
