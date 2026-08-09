// pipeline {
//       agent { label 'AGENT-1' }
//     stages {
//         stage('Build') {
//             steps {
//                 script{
//                     sh """
//                     echo "Hello, this is build"
//                     """
//                 }
//             }
//         }
//         stage('Test') {
//             steps {
//                 script{
//                     sh """
//                     echo "Hello, this is test"
//                     """
//                 }
//             }
//         }
//         stage('Deploy') {
//             steps {
//                 script{
//                     sh """
//                     echo "Hello, this is deploy"
//                     """
//                 }
//             }
//         }
//         post { 
//         always { 
//             echo 'I will always say Hello again!'
//         }
//     }
//     failure { 
//         always { 
//             echo 'I will run when pipeline is failed!'
//         }
//     }
//     success { 
//         always { 
//             echo 'I will run when pipeline is successful!'
//         }
//     }
//     }
// }




pipeline {
    agent {
    
        label 'AGENT-1' }
        environment { 
           PROJECT = 'EXPENSE'
           COMPONENT = 'BACKEND'
    }
    
    options { 
        disableConcurrentBuilds()
         
         timeout(time: 30, unit: 'MINUTES')
    }
    stages {

        stage('Build') {
            steps {
                script {
                    sh """
                        echo "Hello, this is build"
                        echo "PROJECT: $PROJECT"
                        sleep 15
                    """
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    sh """
                        echo "Hello, this is test"
                    """
                }
            }
        }

        stage('Deploy') {
            steps {
                script {
                    sh """
                        echo "Hello, this is deploy"
                    
                    """
                }
            }
        }
    }

    post {
        always {
            echo 'I will always say Hello again!'
        }

        failure {
            echo 'I will run when pipeline is failed!'
        }

        success {
            echo 'I will run when pipeline is successful!'
        }
    }
}