pipeline {
    agent any
    stages {
        stage("Set Gradle Permissions") { // 새로운 단계 추가
            steps {
                sh 'chmod +x gradlew' // gradlew 파일에 실행 권한 부여
            }
        }
        stage("Compile") {
            steps {
                sh "./gradlew compileJava"
            }
        }
        stage("Build") {
            steps {
                sh "./gradlew build"
            }
        }
        stage("Unit test") {
            steps {
                sh "./gradlew test"
            }
        }
    }
}
