pipeline{
  agent any
  stages {
    stage ("build") {
      steps {
        echo "Running build automation..."
        sh 'cat gradle/wrapper/gradle-wrapper.properties'
        sh './gradlew build --no-daemon'
        archiveArtifacts artifacts: 'dist/trainSchedule.zip'
      }
    }
  }
}
