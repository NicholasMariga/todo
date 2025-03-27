pipeline{
    agent any
    tools {
        gradle "gradle"
    }
    stages{
        stage("Cloning repository"){
          steps{
                git branch:'master', url:'https://github.com/NicholasMariga/todo.git'
            }
        }
        
        stage("Building code"){
            steps{
                sh "gradle build"
            }
        }
        
        stage("Testing code"){
            steps{
                sh "gradle test"
            }
        }
        stage("Archive"){
            steps{
                sh "echo 'Archiving the build'"
            }
        }
    }
}
