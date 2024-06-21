pipeline {
  agent {
    label {
      label "built-in"
      customWorkspace "/mnt/test" }
  }
  stages {
    stage ("Git") {
      steps {
        sh 'yum install git -y' }
    }
     stage ('Maven') {
            steps {
                dir ("/root/build-tool") {  
                  rm -rf *
                sh 'wget https://dlcdn.apache.org/maven/maven-3/3.9.8/binaries/apache-maven-3.9.8-bin.zip'
                 sh 'unzip apache-maven-3.9.8-bin.zip'
                  sh 'rm -rf apache-maven-3.9.8-bin.zip'
                  sh 'mvn -version'
                  sh 'rm -rf /root/.m2/' 
                }
            }
        }
  }
}
