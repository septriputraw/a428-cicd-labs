// install nodejs and build  app using scripted pipeline 

node {
    withDockerContainer(args: '-p 3000:3000', image: 'node:16-buster-slim') {
        // inside the container
        stage('Build') {
            checkout scm
            sh 'npm install'
        }
    }
}