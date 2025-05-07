pipeline {
    agent any
 
    triggers {
        cron('* * * * *') // Runs every 1 minute
        //cron(*/5 * * * *) // Runs every 5 minutes
        //cron(*/10 * * * *) // Runs every 10 minutes
        //cron(*/15 * * * *) // Runs every 15 minutes
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
 
