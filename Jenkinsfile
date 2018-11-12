properties([pipelineTriggers([githubPush()])])
node('linux') {
    git url: 'https://github.com/XiongVang/infrastructure-pipeline.git', branch: 'master'

    stage ("GetInstances") {
        sh "aws ec2 describe-instances --region us-east-1"
    }

    stage ("CreateInstance") {
        sh "aws ec2 run-instances --image-id ami-013be31976ca2c322 --count 1 --instance-type t2.micro --key-name seis665 --security-group-ids ssg-72b78539 --subnet-id subnet-ad09a683 --region us-east-1"
    }
}
