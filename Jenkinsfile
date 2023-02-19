pipeline{
  agent any
  stages {
    stage('Build'){
      steps{
        sh 'g++ newhelo.cpp'
        build job : 'PES1UG20CS381-1'
        echo 'built'
      }
    }
    stage('Test'){
      steps{
        sh './a.out'
        echo 'Tested'
      }
    }
  }
  post{
    failure{
      echo 'pipeline has Failed'
    }
  }
}
