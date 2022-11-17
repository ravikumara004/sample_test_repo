pipeline {
    agent any
    parameters {
    choice choices: [
        'a',
        'b', 
        'c', 
        'd'], description: 'select', name: 'Domain'
    choice choices: [
        'urlA', 
        'urlB', 
        'UrlC',
        'UrlD'], description: 'slect url', name: 'url'
    booleanParam defaultValue: true, 
    name: 'dry_run'
    string defaultValue: 'abcd', 
    name: 'Name'
    }

    stages {
        stage('clone') {
            steps {
                echo "hello"
                withCredentials([usernamePassword(credentialsId: 'ghp_9hZPQD', passwordVariable: 'pass', usernameVariable: 'user')]) {
                sh 'git clone https://github.com/ravikumara004/sample_test_repo.git'
                }
                
                script {
                    
                    echo "before"
                    cleanWs()
                    
                }
               }
           }
        stage('clone') {
            steps {
                sh 'echo "ravi"'
            }
        }
    
    }
}
