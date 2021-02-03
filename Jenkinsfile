pipeline{

    agent any

// uncomment the following lines by removing /* and */ to enable
    tools{
       maven 'maven' 
    }
    

    stages{
        stage('one'){
            steps{
                echo 'this is the build job'
                sh 'mvn compile'
            }
        }
        stage('two'){
            steps{
                echo 'this is the test job'
                sh 'mvn clean test'
            }
        }
        stage('three'){
            steps{
                echo 'this is the package job'
                sh 'mvn package -DskipTests'
            }
        }
    }
    
    post{
        always{
            echo 'this pipeline has completed...'
        }
        
    }
    
}
