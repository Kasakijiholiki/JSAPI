pipeline {
    agent any
    stages {
         stage('Build') {
            steps {
             sh 'npm install --save-dev jest'
             sh 'npm i -D jest-sonar-reporter'
             }
        }
        stage('Test') {
            steps {
             sh 'npm test -- --coverage'
             }
        }
    }
/*    post {
        always {
           sh 'sonar-scanner \
  -Dsonar.projectKey=JavaScriptAPI \
  -Dsonar.sources=. \
  -Dsonar.host.url=http://localhost:9000 \
  -Dsonar.login=d1a38684f10325c02003c37733c787cedb2bd6f9'
        }
    
    }
    */
}
