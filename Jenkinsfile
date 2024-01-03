// Meaningless change to justify opening a PR

pipeline {
  agent any

  options {
    timeout([time: 10, unit: 'MINUTES'])
    skipStagesAfterUnstable()
  }

  stages {
    stage('Build') {
      steps {
        script {
          echo """\
            Env:
              * BRANCH_NAME: ${env.BRANCH_NAME}
              * BRANCH_IS_PRIMARY: ${env.BRANCH_IS_PRIMARY}
              * CHANGE_ID: ${env.CHANGE_ID}
              * CHANGE_TITLE: ${env.CHANGE_TITLE}
              * CHANGE_TARGET: ${env.CHANGE_TARGET}
              * CHANGE_BRANCH: ${env.CHANGE_BRANCH}
          """.stripIndent()
        }
      }
    }
  }
}
