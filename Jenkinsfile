pipeline{
    agent any
    tools{
        gradle 'gradle'
    }
        stages{
            stage('clone repository'){
                steps{
                    git branch: 'master', url: 'https://github.com/Barusei/gallery.git'
                }
            }
            stage('build1'){
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