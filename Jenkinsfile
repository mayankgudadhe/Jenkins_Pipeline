pipeline {
  agent {
    label {
      label "built-in"
      customWorkspace "/mnt/test" }
  }
  stages {
    stage ("Git") {
      steps {
      sh 'rm -rf *' }
    }
     stage ('Maven') {
            steps {
                dir ("/root/build-tool") {  
                 sh 'rm -rf *
                  sh 'rm -rf /root/.m2/' 
                }
            }
        }
  }
}
