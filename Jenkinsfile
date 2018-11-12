properties([pipelineTriggers([githubPush()])])
node('linux') {
    git url: 'https://github.com/XiongVang/infrastructure-pipeline.git', branch: 'master'
    stage ("GetInstances") {
        sh "aws ec2 describe-instances --region us-east-1"
    }
}
