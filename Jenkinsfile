pipeline {
    agent any
 
    triggers {
        cron('* * * * *') // Runs every 1 minute
    }
 
    stages {
        stage('Folder Pieline  Job') {
            parallel {
                stage('Job 1') {
                    steps {
                        withCredentials([conjurSecretCredential(credentialsId: 'backup-credential', variable: 'CONJUR_SECRET')]) {
                            sh 'echo Running parallel Job 1 with $CONJUR_SECRET'
                        }
                    }
                }
                stage('Job 2') {
                    steps {
                        withCredentials([conjurSecretCredential(credentialsId: 'backup-credential', variable: 'CONJUR_SECRET')]) {
                            sh 'echo Running parallel job 2 with $CONJUR_SECRET'
                        }
                    }
                }
                
            }}}}
 
