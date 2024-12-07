pipeline {
    agent any  // Defines an agent to execute the pipeline (can be any available agent)
    stages {
        stage('Clone Repository') {  // Step 1: Pull the code from GitHub
            steps {
                git branch: 'main', url: 'https://github.com/nirBSH/TestJenkins.git'
            }
        }
        stage('Install Dependencies') {  // Step 2: Install dependencies
            steps {
                bat 'pip install pytest'  // Install pytest
            }
        }
        stage('Run Tests') {  // Step 3: Run tests
            steps {
                bat 'pytest test.py'  // Run pytest on test.py
            }
        }
    }
}
