pipeline {
    agent any

    stages {
        stage('Deploy') {
            steps {
                bat '"C:\\Users\\USER\\AppData\\Local\\Programs\\DockerDesktop\\resources\\bin\\docker.exe" build -t myweb .'
                bat '"C:\\Users\\USER\\AppData\\Local\\Programs\\DockerDesktop\\resources\\bin\\docker.exe" rm -f myweb-container || exit /b 0'
                bat '"C:\\Users\\USER\\AppData\\Local\\Programs\\DockerDesktop\\resources\\bin\\docker.exe" run -d --name myweb-container -p 8082:80 myweb'
            }
        }
    }
}
