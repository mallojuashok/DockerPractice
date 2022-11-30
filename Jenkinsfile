parameters{
    agent {label 'OPENJDL-11-JDK'}
    stages{
        stage('VCS'){
            steps{
                git branch :"main" ,url:'https://github.com/mallojuashok/DockerPractice.git'
            }
        }
        stage('BUILD'){
            steps{
                sh "docker image build -t spc_pet:1.0"
            }
        }
        stage('Container'){
            steps{
                sh "docker container run --name spring -d -P spc_pet:1.0"
            }
        }
}
}