pipeline{
    agent any
    stages{
        stage('build'){
            steps {
                build 'PES1UG21CS101-1'
                sh 'non_existing_command'
                sh 'g++ main.cpp -o output'
            }

        }
        stage('test'){
            steps{
                sh './output'
            }
        }
        stage('deploy'){
            steps{
                echo 'deploy'
            }
        }
    }
    post{
            failure{
                echo 'pipeline failed'
            }
    }
}
