pipeline {
    agent any

    tools {
        // Install the Maven version configured and add it to the path.
        maven "Maven"
    }

    stages {
        stage('Build') {
            steps {
                // Get code from the GitHub repository
                checkout scmGit(branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/parthjindal50/HelloWorld']])

                // Run Maven commands.
                sh "mvn clean install"
            }
        }
    }
}
