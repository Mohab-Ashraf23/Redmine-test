pipeline{

 agent {
 label "Redmine"
  }

 stages{

   stage("Build"){

     steps{

      sh "cd redmine/jobs"
      sh "mkdir ${env.BUILD_NUMBER}"
      sh "cd ${env.BUILD_NUMBER}"
      sh "git clone git@github.com:Mohab-eSpace/Redmine-test.git"
      sh "cd /var/lib/jenkins/redmine"
      sh "rm -f public"
      sh "ln -s jobs/${env.BUILD_NUMBER} public"

    }
  }
 }
}
