pipeline
{
agent any
stages
{
   stage ('scm checkout')
    {
      steps{
            git branch: 'main', url: 'https://github.com/shafique2710/my-maven-project.git'
            }
     }
    stage ('package the source code')
    {
      steps{
            withMaven(globalMavenSettingsConfig: 'null', jdk: 'JAVA', maven: 'MAVEN', mavenSettingsConfig: 'null') {
            sh 'package'
              }
            }
    }

    stage ('package the source code')
     {
       steps{
            ansiblePlaybook become: true, credentialsId: 'ansible', installation: 'ANSIBLE', inventory: '/etc/ansible', playbook: '/opt/playbooks'
            }
      }
}
}
