pipeline
{
  agent any
  stages
  {
    stage ('scm checkout')
    {
      steps
      { git branch: 'master', url: 'https://github.com/prakashk0301/maven-project' }
    }
  
    
    stage ('Code Package')
    {
      steps
      { withMaven(globalMavenSettingsConfig: 'a21b4ed8-8cda-4b77-9a9f-89e6fdcc408b', jdk: 'MyJDK', maven: 'MyMaven') {
    bat 'mvn package' }
      }
    }
    
    /*
    stage ('Code Compile')
    {
      steps
      { withMaven(globalMavenSettingsConfig: 'a21b4ed8-8cda-4b77-9a9f-89e6fdcc408b', jdk: 'MyJDK', maven: 'MyMaven', mavenSettingsConfig: '554637f6-7f4e-494f-9d86-37a449189b91') {
    sh 'mvn compile' }
      }
    }
  
    
    
    stage ('code build')
    { steps
     { withMaven(globalMavenSettingsConfig: '193254ea-0e8f-4a50-ab38-d01a7d57b6bb', jdk: 'JDK_HOME', maven: 'MVN_HOME') 
      { sh 'mvn package' }
     }
    }
    
    stage ('publish artifact to ansible master server')
    {steps 
     { sshPublisher(publishers: [sshPublisherDesc(configName: 'ansible-master', transfers: [sshTransfer(cleanRemote: false, excludes: '', execCommand: '', execTimeout: 120000, flatten: false, makeEmptyDirs: false, noDefaultExcludes: false, patternSeparator: '[, ]+', remoteDirectory: '//etc//ansible//playbooks', remoteDirectorySDF: false, removePrefix: '', sourceFiles: 'webapp/target/webapp.war')], usePromotionTimestamp: false, useWorkspaceInPromotion: false, verbose: false)])}}
    
    
    stage ('publish deploy-cicd-playbook to ansible master server ')
    {steps 
     { sshPublisher(publishers: [sshPublisherDesc(configName: 'ansible-master', transfers: [sshTransfer(cleanRemote: false, excludes: '', execCommand: '', execTimeout: 120000, flatten: false, makeEmptyDirs: false, noDefaultExcludes: false, patternSeparator: '[, ]+', remoteDirectory: '//etc//ansible//playbooks', remoteDirectorySDF: false, removePrefix: '', sourceFiles: 'deploy-cicd.yaml')], usePromotionTimestamp: false, useWorkspaceInPromotion: false, verbose: false)]) }}
    
    stage ('run playbook')
    {steps 
     {sshPublisher(publishers: [sshPublisherDesc(configName: 'ansible-master', transfers: [sshTransfer(cleanRemote: false, excludes: '', execCommand: 'ansible-playbook /etc/ansible/playbooks/deploy-cicd.yaml', execTimeout: 120000, flatten: false, makeEmptyDirs: false, noDefaultExcludes: false, patternSeparator: '[, ]+', remoteDirectory: '', remoteDirectorySDF: false, removePrefix: '', sourceFiles: '')], usePromotionTimestamp: false, useWorkspaceInPromotion: false, verbose: false)])}}
  */
  
  }
}
       
