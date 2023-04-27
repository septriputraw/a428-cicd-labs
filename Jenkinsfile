// install nodejs and build  app using scripted pipeline 

node {
    docker {
            image 'node:lts-bullseye-slim' 
            args '-p 3000:3000' 
        }
    stage('Build') {
        sh 'npm install'
    }
}