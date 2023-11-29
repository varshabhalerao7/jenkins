pipeline {

  label {
  label 'built-in' 
  customWorkspace '/mnt/vsk'

  }
stages {

  stage ('1st') {
  steps {

*************
    
  }

    stage ('2nd') {
    steps {
               sh "yum install httpd -y"
               sh "chmod -R 777 /var
               sh " cp /mnt/vsk/index.html /var/www/html
    }
    }

stage ('3rd') {
  steps { 
                  sh "service httpd restart"
  }
      

    
  
  
}
  
  }
}
