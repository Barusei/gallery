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
                    sh 'gradle build'
                }
            }
            stage('test'){
                steps{
                    sh 'gradle testing'
                }
            }
        }
}