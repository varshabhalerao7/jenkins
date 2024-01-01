pipeline {

  agent {
    label{
      label 'built-in'
      customWorkspace '/mnt/docker/q1'
    }
  }
stages {
  stage ('docker create-q1-branch') {
steps { git url:"https://github.com/varshabhalerao7/jenkins.git", branch:"q1"

  }
        }
stage ('create docker container') {
steps {
sh "docker run --name b1 -itdp 80:80 httpd"
  
}
}

  stage ('deploy-index') {
    steps {
  sh "chmod -R 777 index.html"
					sh "docker cp index.html b1:/usr/local/apache2/htdocs"
}
}



}
}
