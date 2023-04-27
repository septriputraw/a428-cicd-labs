// install nodejs and build  app using scripted pipeline 

node {
    stage('Install NodeJS') {
        def nodeJSHome = tool name: 'nodejs', type: 'jenkins.plugins.nodejs.tools.NodeJSInstallation'
        env.PATH = "${nodeJSHome}/bin:${env.PATH}"
    }
    stage('Build') {
        sh 'npm install'
    }
}