pipeline {
    agent any
    options {
        office365ConnectorWebhooks([
            [name: "Office 365", url: "${https://camara1.webhook.office.com/webhookb2/b2941e37-7353-480f-85cb-1a1c7c3f9525@6e68e6a6-4d6b-4505-9622-fddaf8cfc755/IncomingWebhook/e4b97fcc110d46d194f319430aecc10e/40f87186-962a-4c5b-bb6c-985ed62744e0}", notifyBackToNormal: true, notifyFailure: true, notifyRepeatedFailure: true, notifySuccess: true, notifyAborted: true]
        ])
    }
    environment {
        BRANCH = 'Master'
    }
    stages {
        stage('Build') {
            environment{
                VARIAVEL = 'variavel'
            }
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
                office365ConnectorSend webhookUrl: "${https://camara1.webhook.office.com/webhookb2/b2941e37-7353-480f-85cb-1a1c7c3f9525@6e68e6a6-4d6b-4505-9622-fddaf8cfc755/IncomingWebhook/e4b97fcc110d46d194f319430aecc10e/40f87186-962a-4c5b-bb6c-985ed62744e0}",
                message: 'Code is deployed',
                status: 'Success' 
            }
        }
    }
}
