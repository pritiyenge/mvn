node {
   stage('download') 
{
    git 'https://github.com/rakya07/mvn.git'
}
stage('build') 
{
    sh 'mvn package'
}
stage('deploy') 
{
   deploy adapters: [tomcat8(credentialsId: 'admin', path: '', url: 'http://172.31.22.68:8080/')], contextPath: 'demo', onFailure: false, war: '**/*.war'
}
}
