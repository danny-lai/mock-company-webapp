pipeline {
  /*
   * TODO: Implement pipeline stages/steps
   *   See documentation: https://www.jenkins.io/doc/book/pipeline/syntax/#stages
   */
   agent any
   tools {
    nodejs '1.6.1'
   }
   stages {
    // stage ('checkoutSource') {
    //     sh "cp -r /github/workspace/* $WORKSPACE"
    // }
    stage('Build') {
      steps {
        // sh 'node -v'
        // sh 'javac -version'

        echo "pipeline build"

        // echo "JAVA_HOME = $JAVA_HOME"
        // echo "JAVA_HOME_8_X64 = $JAVA_HOME_8_X64"
        // def JAVA_HOME = "$JAVA_HOME_8_X64"

        sh './gradlew assemble'
        // sh """
        //   JAVA_HOME=${env.JAVA_HOME_8_X64} ./gradlew assemble
        // """
      }
    }
    stage('Test') {
      steps {
        // sh 'node -v'
        // sh 'javac -version'
        echo "pipeline run tests..."
        
        sh './gradlew test --info'

        // sh """
        //   JAVA_HOME=${env.JAVA_HOME_8_X64} ./gradlew test
        // """
      }
    }
   }
}
