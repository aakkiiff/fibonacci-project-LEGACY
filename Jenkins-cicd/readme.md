1.have kubectl,docker,eksctl,awscli installed on jenkins server
2.add github webhook to trigger jenkins build on commit/user ngrok if using local machine https://youtu.be/adVWQc8T9qg
3.eks kubeconfig update
4.aws configure on the server && server iam authorization eksctl create iamidentitymapping --cluster test001(clustername) --region=ap-south-1 --arn arn:aws:iam::137440810107:role/codebuild-test0-service-role --group system:masters --no-duplicate-arns
5.