
timeout(time: 20, unit: 'MINUTES') {
timestamps {
ansiColor('xterm') {

node('docker')
{
    settingVars()

        stage('build') {
            sh script:
            '''
               echo "Just Something
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

