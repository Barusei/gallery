pipeline{
    agent any
    stages{
        stage('clone repository'){
            steps{
                checkout scmGit(branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/Barusei/gallery.git']])
            }
        }
        stage('build'){
            steps{
             Nodejs('node')
                sh 'npm install'
                sh 'node server.js'
            }
        }
        stage('test'){
            steps{
               Nodejs('node') 
                sh 'npm run rest'
            }
        }
    }
}