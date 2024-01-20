pipeline{

agent { node { label 'workstation' } }


stages{

  stage('build'){
    steps{
      sh 'npm install'
      echo 'build'
    }
}
  stage('unit test'){
      steps{
      // sh 'npm test'
        echo 'unit test'
      }
  }
  stage('code analysis'){
      steps{
        echo 'code analysis'
        sh 'sonar-scanner -Dsonar.host.url= http://172.31.86.197:900' -Dsonar.login= admin -DSonar.password=admin123 -Dsonar.projectKey=cart'
      }
  }

  stage('security scans'){
      steps{
        echo 'security scans'
      }
  }

  stage('artifact creation'){
      steps{
        echo 'artifact creation'
      }
  }

}
}