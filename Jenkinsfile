pipeline{
    agent any
    environment{
        local = "local_pavan"
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
            }
            steps{
                script{
                env.GENDER = "male"
                }
                echo "local variables : ${env.age} ${env.name}"
                echo env.GENDER
                echo AGE
            }
        }
    }
}
    
