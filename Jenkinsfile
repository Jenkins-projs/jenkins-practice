pipeline{
    agent any
    environment{
        local = "local_pavan"
    }
    parameters{
        string(name : 'DEPLOY_ENV' , defaultValue = 'DEV' ,description = 'select the env to deploy')
    }
    stages{
        stage("env"){
            steps{
                echo "local variables : ${env.local}"
            }
        }
    
        stage("env-1"){
            environment{
                age =21
                GIT_COMMIT_SHORT = sh(
                        script: "printf \$(git rev-parse --short ${GIT_COMMIT})",
                        returnStdout: true
                    )
              //  GIT_HOME = tool name: args.git, type: 'git'
            }
            steps{
                script{
                env.GENDER = "male"
                }
                echo "local variables : ${env.age} ${env.name}"
                echo env.GENDER
                echo AGE
                echo env.GIT_HOME
            }
        }
    }
}
    
