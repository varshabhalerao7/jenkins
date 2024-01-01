pipeline {

agent {
label {
label 'built-in'
customWorkspace '/mnt/docker'
}
}

stages {
stage ('creat dir') {
steps {
dir ('/mnt/docker' ) {

  sh "mkdir q2"
}
}
}

  stage ('create container') {

    steps {

      sh "docker run --name q2 -itdp 8080:8080 httpd"

}
}

  stage ('deploy') {

    steps {
   sh "chmod -R 777 index.html"
      sh "docker cp index.html q2:/usr/local/apache2/htdocs"
      
    }
  }
}
}
