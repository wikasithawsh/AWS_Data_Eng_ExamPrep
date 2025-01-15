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
