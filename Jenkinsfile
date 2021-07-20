node {
   stage('Test') {
     checkout scm
     sh "git config remote.origin.fetch '+refs/heads/*:refs/remotes/origin/*'"
     sh "git fetch --all"
     sh "echo Hello World"
   }
}
