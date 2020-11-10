pipeline{

    agent any

// uncomment the following lines by removing /* and */ to enable
    tools{
       maven 'maven' 
    }
    

    stages{
        stage('build'){
            steps{
                echo 'this is the build job for lagairogo-shopping-cart'
                sh 'mvn compile'
            }
        }
        stage('test'){
            steps{
                echo 'this is the test job for lagairogo-shopping-cart'
                sh 'mvn test'
            }
        }
        stage('package'){
            steps{
                echo 'this is the package job for lagairogo-shopping-cart'
                sh 'mvn package'
            }
        }
    }
    
    post{
        always{
            echo 'this pipeline has completed...'
        }
        
    }
    
}
