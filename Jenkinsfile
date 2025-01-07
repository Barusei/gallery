pipeline{
    agent any
    tools {nodejs 'node'}
    stages{
        stage('clone repository'){
            steps{
                checkout scmGit(branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/Barusei/gallery.git']])
            }
        }
        stage('build'){
            steps{
                git 'https://github.com/Barusei/gallery.git'
                sh 'npm install'
                sh 'node server.js'
            }
        }
        stage('test'){
            steps{
                sh 'npm run rest'
            }
        }
    }
}