pipeline{
    agent any
    stages{
        stage('Build'){
            steps{
                sh 'g++ -c PES1UG20CS613.cpp'
                sh 'g++ -o PES1UG20CS613 PES1UG20CS613.cpp'
                echo 'Build Stage Successfull'
            }
        }
        stage('Test'){
            steps{
                sh './PES1UG20CS613'
                echo 'Test stage Executed Successfully'
            }
        }
        stage('Deploy'){
            steps{
                echo 'Deployed Successfully'
            }
        }
    }
    post{
        failure{
            echo 'Pipeline Failed'
        }
    }
}
