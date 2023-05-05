pipeline {
    agent any
    environment {
         DIRECTORY_PATH = "The path of the code directory being fetched."
         TESTING_ENVIRONMENT = "Deploy the application to RuofengQIU's testing environment."
         PRODUCTION_ENVIRONMENT = "Deploy the code to the RuofengQIU's production environment."
    }

    stages {
        stage("Build") {
            steps {
                echo "$DIRECTORY_PATH"
                bat "echo 'Compile the code and generate any necessary artifacts'"
            }
        }
        
        stage('Test') {
            steps {
                echo 'Unit Test'
                bat "echo 'Integration Tests'"
            }
        }
        
        stage('Code Quality Check') {
            steps {
               echo "CHECK"
            }
            post {
                always {
                    echo "Check the quality of the code"
                 }
            } 
        }
        
        stage('Deploy') {
            steps {
                echo "$TESTING_ENVIRONMENT"
            }
        }
        
        stage('Approval') {
            steps {
                echo 'Start'
                sleep(10)
                echo "Continue"
            }
        }
        
        stage('Deploy to Production') {
            steps {
                echo "$PRODUCTION_ENVIRONMENT"
            }
        }  
    }
}
