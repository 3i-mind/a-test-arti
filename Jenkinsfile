
timeout(time: 20, unit: 'MINUTES') {
timestamps {
ansiColor('xterm') {

node('docker')
{
    settingVars([version: '1.0.0'])

        stage('build') {
            sh script:
            '''
               echo "Just Something"
            '''
        }

    stage('Build Docker Image ') {
        buildDocker()
    }

    stage('Push To Registry') {
        pushDkrToArtifactory()
    }

    stage('Cleaning'){
       sh "docker system prune -f"
    }
}

}
}
}

