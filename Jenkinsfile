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
                    reuseNode true
                }
            }
            steps{
                stage("install"){
                    steps{
                        sh 'npm install'
                    }
                }
                stage("test"){
                    steps{
                        sh 'npm run test'
                    }
                }
            }
        }
    }

}
