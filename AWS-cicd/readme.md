help1: https://docs.aws.amazon.com/eks/latest/userguide/add-user-role.html

role name: codebuild-test0-service-role(your code build role name)

<!-- add to cluster the role!: kubectl edit -n kube-system configmap/aws-auth -->
add the code build role to your cluster:

eksctl create iamidentitymapping --cluster test001(clustername) --region=ap-south-1 --arn arn:aws:iam::137440810107:role/codebuild-test0-service-role --group system:masters --no-duplicate-arns

