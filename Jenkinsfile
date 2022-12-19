pipeline{
    agent any
    triggers {
        pollSCM('* * * * *')
    }
    stages {
        stage('vcs'){
            steps {
                git branch:'main',url:'https://github.com/Mypracticeclassoct-dec/saleor-core.git'             
            }
        }
        stage('docker image build'){
            steps {
                sh 'docker image build -t vamsibakka/saleor-core:DEV .'
            }

        }
        stage('push image'){
            steps {
                sh 'docker image push vamsibakka/saleor-core:DEV'
            }
        }
    }
}