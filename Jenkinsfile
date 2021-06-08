pipeline{

    agent any

    tools{
       maven 'Maven 3.6.3' 
    }
    

    stages{
        stage('build'){
            steps{
                echo 'compiling sysfoo app'
                sh 'mvn compile'
            }
        }
        stage('test'){
            steps{
                echo 'running unit test'
                sh 'mvn clean test'
            }
        }
        stage('package'){
            steps{
                echo 'packaging app into a war file'
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
