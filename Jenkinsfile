// install nodejs and build  app using scripted pipeline 

node {
    withDockerContainer(args: '-p 3000:3000', image: 'node:16-buster-slim') {
        // inside the container
        stage('Build') {
            checkout scm
            sh 'npm install'
        }
        stage('Test') {
            checkout scm
            sh './jenkins/scripts/test.sh'
        }
        stage('Deploy') {
            checkout scm
            sh './jenkins/scripts/deliver.sh'
            input message: 'Sudah selesai menggunakan React App? (Klik "Proceed" untuk mengakhiri)'
            sh './jenkins/scripts/kill.sh'
        }
    }
}