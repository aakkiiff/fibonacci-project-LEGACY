1.have kubectl,docker,eksctl,awscli installed on jenkins server
2.add github webhook to trigger jenkins build on commit/user ngrok if using local machine https://youtu.be/adVWQc8T9qg
3.eks kubeconfig update
4.aws configure on the server && server iam authorization eksctl create iamidentitymapping --cluster test001(clustername) --region=ap-south-1 --arn arn:aws:iam::137440810107:role/codebuild-test0-service-role --group system:masters --no-duplicate-arns
5.being it the first version :
    there are some caviate in this sc.
    1.u need to manually paste the jenkins pipeline code to jenkins console and configure pipeline
    2.all docker build commands are considered jenkins-cicd as root dir.but i merged all of them into fibonacci project 
    directory.thus when jenkins runs its job it considers fibonacci project as its root.so ill update these as soon as i can.

    ps.these grp of projects are done seperately and merged into one ,so there are some context issues.