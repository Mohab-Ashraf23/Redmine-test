pipeline{

 agent {
 label "Redmine"
   }

 stages{

   stage("Build"){

     steps{

      sh "cd /var/lib/jenkins/redmine/jobs ; mkdir  ${env.BUILD_NUMBER} ; cd ${env.BUILD_NUMBER}  ; git clone git@github.com:Mohab-eSpace/Redmine-test.git ; mv Redmine-test/* . ; rm -fr Redmine-test"

      sh "cd /var/lib/jenkins/redmine  ; rm -f public ; ln -s jobs/${env.BUILD_NUMBER} public"


    }
  }
 }
}
