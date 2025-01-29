## AWS Lambda note
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
