pipeline  {
  agent any
  stages  {
    stage("run frontend")  {
      steps  {
        echo 'executing yarn...'
        nodejs('NodeJS-23.2')  {
          sh 'yarn install'
        }
      }
    }
    stage("run backend")  {
      steps  {
        echo 'executing gradle...'
        withGradle()  {
          sh './gradle -v'
        }
      }
    }
  }
}
