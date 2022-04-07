@Library(['github.com/indigo-dc/jenkins-pipeline-library@feature/serviceqa']) _

def projectConfig

pipeline {
    agent any

    stages {
        stage('SQA baseline dynamic stages: wordpress') {
            steps {
                script {
                    projectConfig = pipelineConfig(
                        configFile: './.sqa/config.yml'
                    )
                    buildStages(projectConfig)
                }
            }
            post {
                cleanup {
                    cleanWs()
                }
            }
        }
    }
}
