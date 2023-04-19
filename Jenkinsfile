pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        bat 'echo "Building HTML files"'
        bat 'mkdir build'
        bat 'xcopy /s *.html build\\'
      }
    }
    stage('Deploy') {
      steps {
        publishOverSmb([
          smb('xampp', credentialsId: 'windows_credentials', domain: 'WORKGROUP', shareName: 'html', useWorkspaceInPromotion: false, usePromotionTimestamp: false, flattenFilePaths: false, cleanRemote: false, noDefaultExcludes: false, makeEmptyDirs: false, patternSeparator: '[, ]+', verbose: true)
        ])
      }
    }
  }
}
