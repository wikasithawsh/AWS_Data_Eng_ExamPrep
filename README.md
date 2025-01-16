# AWS_Data_Eng_ExamPrep
## AWS DE exam preparation Hands-on activities 

# 01: ETL Pipeline  : ( Move data from source systems into a data  warehouse )

## 1.1: Extract: 
     Retrieve raw data from source systems, e.g., CRMs. flat files, APIs 
     Ensure data integrity during the extraction phase (Data integrity in ETL extraction is the process of ensuring that data is accurate, consistent, and reliable during 
     the Extract, Transform, Load (ETL) process)
     This can be done in real time or in batches, depending on the requirements 

## 1.2: Transformation : 
      Convert extracted data into a suitable format to save in DWH.
      can involve the possible operations:
        1: Data cleansing (remove duplicates, fix errors)
        2: Data enrichment (improving data by adding additional data from other sources )
        3: format changes (date formatting, string manipulation (concatenation))
        4: Encoding or decoding data
        5: handling missing values 
        
## 1.3: Load: 
        Move transformed data into DWH
        it can be done via batches(all at once) or streaming(as data becomes available)

# 02: Data Lineage
      ![image](https://github.com/user-attachments/assets/491648b0-16af-41e4-9441-9cbb360d5cc3)



# 02: AWS S3

### Create IAM policy and attach into the bucket 
    https://docs.aws.amazon.com/IAM/latest/UserGuide/reference_policies_examples_s3_rw-bucket.html

                   {
                   "Version": "2012-10-17",
                   "Statement": [
                       {
                           "Sid": "ListObjectsInBucket",
                           "Effect": "Allow",
                           "Action": ["s3:ListBucket"],
                           "Resource": ["arn:aws:s3:::bucket-name"]
                       },
                       {
                           "Sid": "AllObjectActions",
                           "Effect": "Allow",
                           "Action": "s3:*Object",
                           "Resource": ["arn:aws:s3:::bucket-name/*"]
                       }
                   ]
               }

  ![image](https://github.com/user-attachments/assets/7d790ff9-909a-46a1-94a7-0392e47cbf2f)

## create user group > create IAM user > add user into group > create policy > attach policy into group 
