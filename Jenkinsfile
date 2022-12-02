parameters{
    agent {label 'OPENJDK-11-JDK'}
    stages{
        stage('GIT'){
            steps{
                git branch :"main" , url:'https://github.com/mallojuashok/DockerPractice.git'
            }
        }
        stage('IMAGE BUILD'){
            steps{
                sh 'docker image build -t spc_pet:1.0 .'
            }
        }
        stage('CONTAINER RUN'){
            steps{
                sh 'docker container run --name spring -d -p 8081:8080 spc_pet:1.0'
            }
        }
}
}