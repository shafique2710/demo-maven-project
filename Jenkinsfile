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
            steps{ withMaven(globalMavenSettingsConfig: 'null', jdk: 'JAVA', maven: 'MAVEN', mavenSettingsConfig: 'null') {
              sh 'mvn package'
            }
                 }
      }
}
}
}
