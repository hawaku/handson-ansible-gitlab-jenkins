node {
   stage('git') {
       checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: '', url: '']]])
    }
    
    stage('deploy dry-run') {
        sh 'rsync -avzn -C --delete . /var/www/html'
    }
    
    stage('deploy') {
        sh 'rsync -avz -C --delete . /var/www/html'
    }
}
