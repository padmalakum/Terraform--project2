# Terraform--project2

In this I am going to create Ec2,S3  through Infrastructure as code using Terraform 

we will create different tf files for variables, ec2,s3,providers,terraform like this

terraform.tf
![image](https://user-images.githubusercontent.com/92623347/236691958-d46d149c-2697-4cf6-88a9-33416d596c3b.png)

providers.tf

![image](https://user-images.githubusercontent.com/92623347/236692000-70921f29-eca6-4e9c-8382-a093adaeffaf.png)

variables.tf

![image](https://user-images.githubusercontent.com/92623347/236692027-eb369db8-60aa-49b9-b01f-525a7f2d6268.png)

servers.tf
![image](https://user-images.githubusercontent.com/92623347/236692061-4c1818d3-1f38-4fa4-a766-096b020e5249.png)

s3.tf

![image](https://user-images.githubusercontent.com/92623347/236692087-5e21e2d4-f866-4656-87bb-dfc405b79c63.png)

output.tf

![image](https://user-images.githubusercontent.com/92623347/236692117-1109d49d-638e-4eda-a04d-d0487200848b.png)

we have to configure aws in our local machine with access keys and secret access keys by creating Iam user .

then perform terraform init, looks like this

![image](https://user-images.githubusercontent.com/92623347/236692471-c8343dd9-6c2d-4451-a526-b6c44e887dd2.png)

terraform plan , it shows like this

![image](https://user-images.githubusercontent.com/92623347/236692519-ff533490-818d-48bd-b2c4-488cdfd0356e.png)

terraform apply
then it will create ec2 server and s3 bucket for us

![image](https://user-images.githubusercontent.com/92623347/236692776-c106ee25-94ef-4861-8cd8-d8e72e6b02c2.png)

![image](https://user-images.githubusercontent.com/92623347/236692817-73ef5a58-a9f5-4227-8443-3a9b8a30a65b.png)

![image](https://user-images.githubusercontent.com/92623347/236692844-87c0892e-e3bf-49fd-b475-a3d87c648f8c.png)

![image](https://user-images.githubusercontent.com/92623347/236692873-234786ad-b8d2-407f-84b1-11bacf01b995.png)

when we run terraform apply then only terraform.tfstate file will be created



