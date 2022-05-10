pipeline {

    agent any



    stages {

        stage('install') {
            steps {
                echo 'Installing...'
                sh 'cd project-name/ && npm install'
            }
        }

        stage('Build') {

            steps {

                echo 'Building..'

                sh 'cd project-name/ && npm run build'
            }

        }

        stage('Test') {

            steps {

                echo 'Testing..'

                sh 'cd project-name/ && npm run test:e2e'

            }

        }

        stage('Deploy') {

            steps {

                echo 'Deploying....'

                sh 'cd project-name/ && npm run start:prod'

            }

        }

    }

}
