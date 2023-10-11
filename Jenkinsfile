pipeline {
    agent any 
environment {
        PATH = "$PATH:/opt/flutter/bin"
    }

    stages {
        stage('clonings') { 
            steps {
               echo "cloning"
               git branch: 'main', credentialsId: '6d6b8627-3201-4abb-be36-cf0c99f80c59', url: 'git@github.com:retailapps/futuretail-switch-admin-frontend.git'
            }
        }
 stage('build web') { 
            steps {
               echo "build"
               sh "flutter --version" 
               sh "cd $WORKSPACE"
               sf "flutter build web"     
                 
            
            }
        }
 
    }
}
