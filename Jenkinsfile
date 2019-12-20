pipeline {
    agent { docker { image 'maven:3.3.3' } }
    stages {
        stage('build') {
            steps {
                scalac Hello.scala
                scala Hello
            }
        }
    }
    post { 
      always {  
        recordIssues enabledForFailure: true, tools: [scala()] 
        } 
    }
}
