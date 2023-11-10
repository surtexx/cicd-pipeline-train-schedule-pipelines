pipeline{
  agent any
  stages {
    stage ("build") {
      steps {
        echo "Running build automation..."
        sh './gradlew wrapper --gradle-version 6.0.1'
        sh './gradlew build --no-daemon'
        archiveArtifacts artifacts: 'dist/trainSchedule.zip'
      }
    }
  }
}
