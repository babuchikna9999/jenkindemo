pipeline{
    agent any

    stages{
        stage("Checkout code"){
            steps{
                Checkout scm
            }
        }

        stage("Extract data"){
            steps{
                bat "python extract.py"
            }
        }
    }

    post{
        success{
            echo "Pipeline successfully executed..."
        }
    }
}