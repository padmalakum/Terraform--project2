After we run terraform apply , it will create terraform.state file will be created

and we can use these commands to see all we have created .

![image](https://user-images.githubusercontent.com/92623347/236693099-a8157ff6-f0df-43cd-9543-0ec3d7173a37.png)

and we can specify instance type to see all of its configuration like this

![image](https://user-images.githubusercontent.com/92623347/236693167-9334aeb6-97f6-4fa2-957b-e30e04ac831a.png)

In terraform we have to maintain code and state file and it is very important to maintain state file .
As we cannot commit state file to git because of security reasons as it will have sensitive date (private ip, account number,arn )
If we change anything in code like bucket name etc, the state will be changes automatically, it will stay in our local machine .

then Remote backend will come into picture 
we have to integrate this state file to remote backend as s3 bucket and database..

If we change anything in code like s3 bucket name then state will be changed automatically
thats why we need to store this state file in remote backend.
it will take s3 bucket and dynamodb as a nosql database.

we need to add backend block in terraform.tf file , where this backend configuration defines  exactly how operations are performed where state snapshots are stored etc.

![image](https://user-images.githubusercontent.com/92623347/236702756-200cf20c-b7a7-474a-b71f-c02d7a3aaa8c.png)

so if all the team members want to change the code then terraform will apply a lock for that particular terraform apply  command until it runs and saves the info (like who changed it.._in the dynamo table

and when that apply is done lock will release on state file sothat others can change.

![image](https://user-images.githubusercontent.com/92623347/236704117-afa62171-fcba-4eac-a3c6-4484c58dfdf0.png)

Now we don't have to keep terraform tfstate in our local machines as this state is remotely backed up in dynamodb

we can create dynamo.tf like this 

![image](https://user-images.githubusercontent.com/92623347/236704185-c37f1f52-23e3-416a-af4a-018e56d22347.png)


