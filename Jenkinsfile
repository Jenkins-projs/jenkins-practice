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
    
