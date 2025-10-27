pipeline{
    agent any
    environment{
        PYTHON='C:\\Users\\shivr\\AppData\\Local\\Programs\\Python\\Python314\\python.exe'
    }
    stages{
        stage("Checkout code"){
            steps{
                checkout scm
            }
        stage("Extract pipeline"){
            steps{
                bat "${env.PYTHON} extract_etl.py"
            }
        }
        }
    }
    post{
        success{
            echo "Success..."
        }
        failure{
            echo "Failure..."
        }
        always{
            echo "Always..."
        }
    }
        

}