pipeline {
agent {
  label {
  label 'built-in' 
  customWorkspace '/mnt/vsk'
  }
  }
stages {

  stage ('1st') {
  steps {

git branch: 'q3', credentialsId: 'git', url: 'https://github.com/varshabhalerao7/jenkins.git'
    
  }
  }

    stage ('2nd') {
    steps {
               sh "yum install httpd -y"
               sh "chmod -R 777 /var/www/html"
               sh " cp /mnt/vsk/index.html /var/www/html"
    }
    }

stage ('3rd') {
  steps { 
                  sh "service httpd restart"
  }
      
 
}
  
  
}
}
