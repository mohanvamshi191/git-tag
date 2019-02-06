pipeline {
    agent any
         stages{
             stage('SCM Checkout'){
                  steps{
                checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/csenapati12/git-tag.git']]]) 
                  }
             }
           stage('Read YAML file') {
             steps {
               script{ 
                   datas = readYaml (file: 'repo.yaml') 
                }
                   echo datas.services.myagent1.repo.toString()

              }
           }
         }
    
}
