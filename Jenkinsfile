pipeline {
    agent {label "agent1"} 
    //tools { maven "maven-3.8.6" }
    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                sh 'mvn clean package'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing nothing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
                }
            }
        }    



    }
}
