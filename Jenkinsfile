pipeline{
    agent any
    stages{
        stage('clone repo'){
            steps{
                git url:"https://github.com/renuka4569/face.git",branch:'main'
            }
        }
        stage ('depenency'){
            steps{
                bat '''
                pythob -m venv venv
                call venv\\script\\active
                python -m pip install --upgrade pip
                pip install pytest
                '''
                }
        }
        stage ('test'){
            steps{
                bat '''
                call venv\\script\\active
                pytest testfile.py
                '''

                }
        }
        stage('deploy'){
            steps{
                bat '''
                call venv\\script\\active
                python hello.py
                '''
                }
            }
        }
    }

    
