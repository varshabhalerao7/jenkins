pipeline {
agent {
  label {
  label 'slave-03' 
  customWorkspace '/mnt/vsk'
  }
  }
stages {

  stage ('1st') {
  steps {

git url: 'https://github.com/varshabhalerao7/jenkins.git'
    
  }
  }

    stage ('2nd') {
    steps {
               sh "sudo yum install httpd -y"
               sh "sudo chmod -R 777 /var/www/html"
               sh "sudo cp /mnt/vsk/index.html /var/www/html"
    }
    }

stage ('3rd') {
  steps { 
                  sh "service httpd restart"
  }
      
 
}
  
  
}
}
