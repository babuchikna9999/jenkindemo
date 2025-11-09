pipeline{
    agent any

    environment{
        PYTHON:"C:\\Users\\Lenovo\\AppData\\Local\\Programs\\Python\\Python314\\python.exe"
    }

    stages{
        stage("Checkout code"){
            steps{
                checkout scm
            }
        }

        stage("checking python version"){
            steps{
                bat "${env.PYTHON} --version"
            }
        }

        stage("Extract data"){
            steps{
                bat "${env.PYTHON} extract.py"
            }
        }
    }

    post{
        success{
            echo "Pipeline successfully executed..."
        }
    }
}