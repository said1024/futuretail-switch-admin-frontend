pipeline {
    agent any 
environment {
        PATH = "$PATH:/opt/flutter/bin"
    }

    stages {
        stage('clonings') { 
            steps {
               echo "cloning"
               git branch: 'main', credentialsId: 'jenkinsTest', url: 'https://github.com/Oualitsen/optidial-front.git'
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
