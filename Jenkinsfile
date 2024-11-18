pipeline  {
  agent any
  tools  {
    gradle 'Gradle-8.11'
  }
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
        sh 'gradle init'
        echo 'executing gradle...'
          sh './gradlew -v'
        }
    }
  }
}
