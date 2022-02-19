CODE_CHANGES = getGitChanges()
pipeline{
    agent any
    environment{
        NEW_VERSION  = '1.3.0'
    }
    parameters{
        string(name: 'VERSION', defaultValue: '', description: "")
        choice(name: 'VERSION', choices: ['1.1.0', '1.2.0', '1.3.0'], description: '')
    }
    tools{
        maven 'Maven'
        // gradle
        // jdk
    }
    stages{
        stage("build"){
            steps{
                echo 'building the application'
                echo "building version ${NEW_VERSION}"
                sh 'mvn install'

            }
        }
    }
    stages{
        stage("test"){
            when{
                expression{
                    BRANCH_NAME == 'master' && CODE_CHANGES == true
                }
            }
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
