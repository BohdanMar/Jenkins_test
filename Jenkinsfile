pipeline {
    agent any
    environment {
        url_name = "${url_name}"
    }
    stages {
        stage('Load shared libs from local repo') {
            steps {
                //library identifier: 'shared-library@thisIsRequiredButIgnored', retriever: legacySCM(scm)
                script{
                    echo "Loading library" //manager.addShortText("BUILD TRIGGERED BY : $BUILD_USER")
                }
            }
    }
      stage('Hello World') {
        steps {
                script{
                     sh '''
                    cd $(mktemp -d)
                    git clone https://github.com/BohdanMar/Jenkins_test.git
                    cd Jenkins_test
                    sh hello.py
                    '''
                }
            }
        }
    }
}

