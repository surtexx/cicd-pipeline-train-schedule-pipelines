pipeline{
  agent any
  stages {
    stage ("build") {
      steps {
        echo "Running build automation..."
        sh "sed 's/https\://services.gradle.org/distributions/gradle-4.6-bin.zip/https\://services.gradle.org/distributions/gradle-8.5-rc-1-bin.zip' gradle/wrapper/gradle-wrapper.properties"
        sh './gradlew build --no-daemon'
        archiveArtifacts artifacts: 'dist/trainSchedule.zip'
      }
    }
  }
}
