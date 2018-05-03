env.PWD_BIND = '/workspace'
env.DIST = 'xenial'
env.TYPE = 'unstable'

node {
   stage('clone') {
      checkout scm
   }
   stage('germinate') {
      sh '~/tooling/nci/contain.rb /workspace/run'
   }
   stage('results') {
      archive '*'
   }
}
