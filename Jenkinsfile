stage('Init') {
  node('linux') {
    checkout scm
    nodejs(nodeJSInstallationName: 'node 8 latest') {
      sh 'npm install --production'
      sh 'npm start'
    }
  }
}
