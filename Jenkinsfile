pipeline{
    agent any
    environment{
        NPM_CONFIG_CACHE = "${WORKSPACE}/.npm"
    }
    stages{
        stage('etapa de construccion de aplicación'){
            agent{
                docker{
                    image 'node:alpine3.20'
                }
            }
            steps{
                stage("install"){
                    steps{
                        sh 'npm install'
                    }
                }
            }
        }
    }

}
