pipeline
{
agent any
stages
{
      stage ('scm checkout')
      {
            steps{ git branch: 'main', url: 'https://github.com/shafique2710/my-maven-project.git'}
       }
      stage ('build and package the src code')
      {
            steps{ withMaven(jdk: 'JAVA', maven: 'MAVEN') {
              sh 'mvn package'
            }
                 }
      }
      stage (' build docker image')
      {
            steps{ sh 'docker build -t sha2710/mytomcat:01 .'}
      }
}
}
