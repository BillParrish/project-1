pipeline {
   
    agent any

    stages{

        stage('Git Checkout'){

            steps{
                git branch: 'main', url: 'https://github.com/BillParrish/project-1.git'
            }
            

        }
        stage('UNIT Testing'){

            steps{
                script{
                    sh 'mvn test'
                }
            }
        }
        stage('Integration Testing'){

            steps{
                script{
                sh 'mvn verify -DskipUnitTests'
                }
            }
        }

    
    }
}