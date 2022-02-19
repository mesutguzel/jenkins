pipeline{
    agent any
    stages{
        stage("build"){
            steps{
                echoo 'building the application'

            }
        }
    }
    stages{
        stage("test"){
            steps{
                echo 'testing application'
            }
        }
    }
    stages{
        stage("deploy"){
            steps{
                echo 'deploying application'
            }
        }
    }
    post{
        always{
            //define sth
        }
        success{
            //define sth
        }
        failure{
            //define sth
        }
    }
}
