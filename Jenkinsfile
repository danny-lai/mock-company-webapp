pipeline {
  /*
   * TODO: Implement pipeline stages/steps
   *   See documentation: https://www.jenkins.io/doc/book/pipeline/syntax/#stages
   */
   agent any
   stages {
    // stage ('checkoutSource') {
    //     sh "cp -r /github/workspace/* $WORKSPACE"
    // }
    stage('Build') {
      steps {
        sh 'node -v'
        sh 'javac -version'
        sh './gradlew assemble'
      }
    }
    stage('Test') {
      steps {
        sh 'node -v'
        sh 'javac -version'
        sh './gradlew test'
      }
    }
   }
}
