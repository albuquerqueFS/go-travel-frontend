pipeline {
  agent any
  tools {nodejs "nodejs"}
  stages {
    stage("Build") {
      steps {
        sh "sudo npm install"
        sh "sudo npm run build"      
      }
    }
    stage("Deploy") {
      steps {
        sh "sudo rm -rf /var/www/go-travel-frontend"
        sh "sudo cp -r ${WORKSPACE}/build/ /var/www/go-travel-frontend/"
      }
    }
  }
}

