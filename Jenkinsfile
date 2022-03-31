pipeline {
    agent any
    stages {
        stage('compile') {
            steps {
                script{
                    echo "compilin the job"
                }
            }
        }
        stage('UnitTest') {
            steps {
                script{
                    echo "Running the test cases"
                }
            }
        }
        stage('package') {
            steps {
                script{
                    echo "Packaging the job"
                }
            }    

        }
    }
}
