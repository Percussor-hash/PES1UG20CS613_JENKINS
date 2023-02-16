pipeline{
    agent any
    stages{
        stage('Build'){
            steps{
                sh 'g++ -c PES1UG20CS000.cpp'
                sh 'g++ -o PES1UG20CS613 PES1UG20CS613.cpp'
                echo 'Build stage successfull'
            }
        }
        stage('Test'){
            steps{
                sh './PES1UG20CS613'
                echo 'Test stage executed successfully'
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
