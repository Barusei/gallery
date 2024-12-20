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
            stage('build'){
                steps{
                    sh 'gradle build 3'
                }
            }
            stage('test'){
                steps{
                    sh 'gradle testing'
                }
            }
        }
}