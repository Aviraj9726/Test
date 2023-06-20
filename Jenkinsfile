pipeline {
  environment {
    dockerimagename = "aviraj3109/custom-httpd"
    dockerImage = ""
  }
  agent any
  stages {
    stage('Checkout Source') {
      steps {
        git 'https://github.com/Aviraj9726/Test.git'
      }
    }
   
  stage('Deploying React.js container to Kubernetes') {
      steps {
        script {
          kubernetesDeploy(configs: "httpd_deploy.yaml", "httpd_svc.yaml")
        }
      }
    }
  }
}
