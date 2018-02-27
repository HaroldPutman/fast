stage('Init') {
  node('linux') {
    checkout scm
    def result
    nodejs(nodeJSInstallationName: 'node 8 latest') {
      sh 'npm install --production'
      result = sh script:'npm start'
      currentBuild.description = result.trim()
    }
  }
}
