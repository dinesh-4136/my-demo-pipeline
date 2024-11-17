pipeline  {
  agent any
  stages  {
    stage("run frontend")  {
      steps  {
        echo 'excuting yarn...'
        nodejs('NodeJS-23.2')  {
          sh 'yarn install'
        }
      }
    }
    stage("run backend")  {
      steps  {
        echo 'excuting gradle...'
        withGradle()  {
          sh './gradlew -v'
        }
      }
    }
  }
}
