stage('Init') {
  node('linux') {
    checkout scm
    def result
    nodejs(nodeJSInstallationName: 'node 8 latest') {
      sh 'npm install --production'
      result = sh script:'npm start', returnStdout:true
      def resultList = result.trim().split('\n')
      currentBuild.description = resultList.last()
    }
  }
}
