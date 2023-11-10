pipeline{
  agent any
  stages {
    stage ("build") {
      steps {
        echo "Running build automation..."
        sh 'export PATH=$PATH:/opt/gradle/gradle-8.4/bin'
        sh 'gradle wrapper --gradle-version=5.1.1'
        sh './gradlew build --no-daemon'
        archiveArtifacts artifacts: 'dist/trainSchedule.zip'
      }
    }
  }
}
