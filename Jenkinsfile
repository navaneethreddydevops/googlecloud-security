pipeline {
    agent any

    stages {
        stage('GitCheckout') {
            steps {
                checkout([$class: 'GitSCM', branches: [[name: '*']], doGenerateSubmoduleConfigurations: false, extensions: [[$class: 'CleanCheckout', deleteUntrackedNestedRepositories: true], pruneTags(true), [$class: 'AuthorInChangelog'], [$class: 'PruneStaleBranch']], submoduleCfg: [], userRemoteConfigs: [[credentialsId: 'Github', url: 'https://github.com/navaneethreddydevops/googlecloud-security.git']]])
            }
        }
        stage('Build'){
            steps{
                sh 'docker system prune -a'
            }
            
        }
        stage('Docker Build'){
            steps{
            input message: 'Please Provide Approval', ok: 'Approve', parameters: [string(defaultValue: 'YES', description: 'Provide the approval', name: 'Approval', trim: true)]
            }
        }
        stage('CleanUp'){
            steps{
                cleanWs disableDeferredWipeout: true, notFailBuild: true
            }
        }
    }
}
