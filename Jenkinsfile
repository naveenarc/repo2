pipeline {
    agent any
    parameters{
        string(name:'Env',defaultValue:'Test',description:'Version to deploy')
        booleanParam(name:'executeTests',defaultValue: true,description:'decide to run tc')
        choice(name:'APPVERSION',choices:['1.1','1.2','1.3'])
    }
    stages {
        stage('compile') {
            steps {
                script{
                    echo "compilin the job"
                }
            }
        }
        stage('UnitTest') {
            when{
                expression{
                    params.executeTests == true
                }
            }
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
        stage('deploy') {
            steps {
                script{
                    echo "Deploying the app"
                    echo "Deploying to env: ${params.env}"
                    echo "Deploying the appversion: ${params.APPVERSION}"
                }
            }    

        }
    }
}
