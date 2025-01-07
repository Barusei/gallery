pipeline{
    agent any
    tools{
        gradle 'gradle'
    }
        stages{
            stage('clone repository'){
                steps{
                    checkout scmGit(branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/Barusei/gallery.git']])
                }
            }
            stage('build'){
                steps{
                    sh 'gradle build'
                }
            }
            stage('test'){
                steps{
                    sh 'gradle test'
                }
            }
        }
}