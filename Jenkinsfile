// pipeline {
//     agent any

//     stages {
//         stage('Setup Python Environment') {
//             steps {
//                 bat '''
//                 python --version
//                 python -m venv venv
//                 venv\\Scripts\\activate
//                 python -m pip install --upgrade pip
//                 pip install -r requirements.txt
//                 '''
//             }
//         }

//         stage('Run Tests') {
//             steps {
//                 bat '''
//                 venv\\Scripts\\activate
//                 pytest
//                 '''
//             }
//         }
//     }
// }
pipeline {
    agent any

    environment {
        PYTHON = "C:\\Users\\karth\\AppData\\Local\\Programs\\Python\\Python313\\python.exe"
    }

    stages {
        stage('Setup Python Environment') {
            steps {
                bat """
                "%PYTHON%" --version
                "%PYTHON%" -m venv venv
                venv\\Scripts\\activate
                "%PYTHON%" -m pip install --upgrade pip
                pip install -r requirements.txt
                """
            }
        }

        stage('Run Tests') {
            steps {
                bat """
                venv\\Scripts\\activate
                pytest
                """
            }
        }
    }
}

