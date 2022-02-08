pipeline
{
agent any
stages
{
      stage ('scm checkout')
       {
        git branch: 'main', url: 'https://github.com/shafique2710/my-maven-project.git'
       }
      stage ('package the source code')
       {
        withMaven(globalMavenSettingsConfig: 'null', jdk: 'JAVA', maven: 'MAVEN', mavenSettingsConfig: 'null') {
        sh 'mvn package'
             }
       }
}
}
