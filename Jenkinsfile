pipeline {

  agent {
    label{
      label 'built-in'
      customWorkspace '/mnt/nnn'
    }
  }
stages {
  stage ('1st-git') {
steps { git branch: 'q2', credentialsId: 'git', url: 'https://github.com/varshabhalerao7/jenkins.git'

  }
        }
stage ('2nd-yum') {

sh "yum install httpd -y"
  sh " cp /mnt/nnn/index.html /var/www/html"
  sh "yum restart httpd"
  
}

}
}
