pipeline{
    agent any
    stages{
        stage('clone repo'){
            steps{
                git credentiaIsID : "demo",url : "https://github.com/renuka4569/face.git",branch:'branch'
            }
        }
        stage ('depenency'){
            steps{
                bat '''
                pythob -m venv venv
                call venu\\script\\active
                python -m pip install --upgrade
                pip install pytest
                }
        }
        stages ('test'){
        steps{
        bat '''
        call venu\\script\\active
        pytest(testfile.py)
            }
        }
        stages('deploy'){
            steps{
                bat '''
                call venu\\script\\active
                python hello.py
                '''
                }
            }
        }
    }

    
