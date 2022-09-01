pipeline {
    agent agent1 
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
                script { 
                deploy adapters: [tomcat9(credentialsId: "2125e680-7b9c-4f74-8ff3-0cbb3c4e2683", path: "", url: "http://localhost:8080")], contextPath: "/pipeline", onFailure: false, war: "**/*.war" 
                }
            }
        }    



    }
}
