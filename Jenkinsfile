pipeline {

agent {
label {
label 'slave-02'
customWorkspace '/mnt/aaa'
}

stages {
stage ('1st-git') {
steps {
git url:"https://github.com/varshabhalerao7/jenkins.git", branch:"q2"
}

stage ('2nd-yum') {

  steps {

    sh "sudo yum install httpd -y"
    sh "chmod -R 777 /var/www/html"
    sh "sudo cp /mnt/aaa/index.html /var/www/html"
    
    sh "sudo service httpd restart"
}
}

}
