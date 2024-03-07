pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                script {
                    // Clone the Git repository
                    sh 'rm -rf Achala_PES1UG21CS027_Jenkins'
                    sh 'git clone https://github.com/Achala-Nayak/Achala_PES1UG21CS027_Jenkins.git'
                }
            }
        }

        stage('Build') {
            steps {
                script {
                    // Move to the repository directory
                    
                        // Compile the C++ code using a shell script
                        sh 'g++ -o PES1UG21CS027-1 hello.cpp'
                    
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    // Move to the repository directory
                    
                        // Print the output of the compiled C++ program
                        sh './PES1UG21CS027-1'
                    
                }
            }
        }

        stage('Deploy') {
            steps {
                script {
                    // You can add deployment steps here
                    echo 'Deployment steps go here'
                }
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
