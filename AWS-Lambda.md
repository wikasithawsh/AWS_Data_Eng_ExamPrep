![image](https://github.com/user-attachments/assets/1dd768bc-ec76-4b77-a197-eda17d68671f)## AWS Lambda note
------------------------------------------------------------------------------
01: What is Lambda \
02: How to create Lambda Function \
03: How to create lambda by uploading zip code file?\
04: How to create lambda by uploading zip code file to S3\
05: Lambda functio URL?\
06: Lambda environment variable\
07: Lambda Layers 
-------------------------------------------------------------------------------
## 01: What is Lambda
Lambda is an executor that takes code as input, executes it, and produces the output.
![image](https://github.com/user-attachments/assets/26c94b1a-ace3-4ce8-8a86-3bf20452621e)

-------------------------------------------------------------------------------
## 02: How to create Lambda Function 

In Lambda we don't need EC2 here.
when we use aws Lambda : 
  no server ste-up \
  no start or stop \
  no additional cost \
  Serverless [ we don't need to use Ec2] \ 

![image](https://github.com/user-attachments/assets/a073c2ee-2a7b-4e12-84d9-a9b1a68af67d)

  ## Steps : 
  1: Create Lambda function and write Python function.\
  2: Test Lambda function > create test event > 

## 03: How to create lambda by uploading zip code file
   ## Steps
   in Vs Code > 
   1: python -m venv venv \
   2: pip3 install -r requirements.txt \
         in requirements.txt >>>
            requests==2.26.0
            boto3==1.20.19
      
   3: test_lambda.py > 
         import json
     
         def lambda_handler(event, context):
             # TODO implement
             print("Lambd from my code")
             return {
                 'statusCode': 200,
                 'body': json.dumps('Hello from Lambda!')


                }
   4: Create a Zip folder for requiremnt.txt & Venv & test_lambda.py 

   5: Upload the zip file created above into AWS Lambda

   6: Change/Edit  Lambda configss > lambda handle function script name (test_lambda)

   7: Test the zip file 
   
   ------------------------------------
   
            import json
         
         def lambda_handler(event, context):
             # TODO implement
             return {
                 'statusCode': 200,
                 'body': json.dumps('Hello from Lambda!')

   ---------------------------------------------

   ## 04: Create lambda by uploading zip code file to S3

   Steps : 
   1: Create S3 bucket & upload zip file 
   ![image](https://github.com/user-attachments/assets/c041a8fe-9ca0-41d0-ab87-445909d896f6)

   2: ![image](https://github.com/user-attachments/assets/3066037b-5004-4cb3-bf77-79c5e7c9cf3d) 

   -----------------------------------------------
  ## 05 Lambda URL 
  This URL is unique to our Lambda function and we can access the lambda function via this URL.

   ![image](https://github.com/user-attachments/assets/19350498-035d-48ad-8534-976bfebb61ea) 

   ![image](https://github.com/user-attachments/assets/8e1472bf-b9e8-4bdd-9375-e4e8b13d922b)

   we can find the Lambda function URL below 
   ![image](https://github.com/user-attachments/assets/308bd9c1-971a-4e90-8703-d0cbed4b2cba)

   ## 5.1: Create Lambda function URL with a more secure method 
   ![image](https://github.com/user-attachments/assets/4829aee3-8b8e-4387-a9ff-00c6db01b297)

   select as AWS IAM
   ![image](https://github.com/user-attachments/assets/5b5dbc23-023e-4ef6-9f59-92dce52b4e41)
      
   ![image](https://github.com/user-attachments/assets/65c169ad-7a36-4d26-bf92-56037264a8ea)
      To access the lambda function URL, we need to provide AWS credentials.

   ## 5.2: Install Postman : 
         sudo snap install postman
   -------------------------------------------------
  ## 6: Environment variables 
   ![image](https://github.com/user-attachments/assets/91ccb714-c088-4cb0-9a1e-e8a1ab12f636)
   
   Now we can use the env variable in lambda code
       ![image](https://github.com/user-attachments/assets/9aa55578-fe00-414c-8c5c-175493ef8f53)

            import json
            import os
            
            def lambda_handler(event, context):
                my_variable_value = os.environ.get('MY_ENV_VARIABLE')
                # TODO implement
                return {
                    'statusCode': 200,
                    'body': json.dumps('AWS Lambda with Env variable! = ' + my_env_variable )

   then Deploy the lambda code & test  
   ## Error occurred : 
 ![image](https://github.com/user-attachments/assets/b54e4cf4-f519-4527-90ef-a320f1f6b8c0)

   ## How to fix the error 

   ![image](https://github.com/user-attachments/assets/62d1f1e1-3e83-45cc-acd9-c60844526c1f)

   Deploy & test now > It's working 
   ![image](https://github.com/user-attachments/assets/8095b1ca-4416-4fbe-8af5-cb8175b5ccb7)

   ![image](https://github.com/user-attachments/assets/5ebd8688-1ce9-4962-8441-cdd71730ba5c)
         

