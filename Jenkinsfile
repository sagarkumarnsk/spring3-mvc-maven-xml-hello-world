pipeline {
    agent any
    stages {
        stage ('get scm') {
            steps 
            { git credentialsId: 'github_credentials',  url: 'https://github.com/sagarkumarnsk/spring3-mvc-maven-xml-hello-world.git'
            }            
        }
        // stage ('maven') {
        //     steps 
        //     { sh 'mvn package'
        //     }            
        // }
        stage ('archieve artifacts') {
            steps 
            { archiveArtifacts 'target/*.war'
            }            
        }
        stage ('email notification') {
            steps 
            { 
                emailext attachLog: true, body: 'Extended Email Notification', subject: 'Extended Email Notification', to: 'sagarkumarnsk1@gmail.com'
            }            
        }
    }
}




