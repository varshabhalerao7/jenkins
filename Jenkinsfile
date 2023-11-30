pipeline {

agent {
label {
label 'slave-02'
customWorkspace '/mnt/aaa'
}

stages {
stage ('1st-git') {
steps {
git url: *****************

}

stage ('2nd-yum') {

  steps {

    sh "yum install httpd -y"
    sh "cp /mnt/aaa/index.html /var/www/html"
    sh "service httpd restart"
}
}

}
