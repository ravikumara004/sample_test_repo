pipeline {
    agent any
    parameters {
    choice choices: [
        'a',
        'b', 
        'c', 
        'd'], description: 'select', name: 'Domain add'
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
                script {
                   cleanWs() //working
                   sh "git clone https://github.com/ravikumara004/sample_test_repo.git" //working
               // 'git branch: 'dev', credentialsId: 'ghp_9hZPQD', url: 'https://github.com/ravikumara004/sample_test_repo.git' //working
                
                   //cleanWs() //working
                }
            }
        }
    }
    stage('MyStage') {
            steps {
                script {
                    try {
                        sh '''
                            echo "hello'
                            echo "hi"
                        '''
                    } catch (Exception e) {
                        echo "Error: ${e.message}"
                    } finally {
                        // Always execute this code, even if there was an error
                        echo "Stage complete"
                    }
                }
            }
        }
}
