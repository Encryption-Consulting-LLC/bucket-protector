# Bucket to Bucket Encryption

Bucket to Bucket Encryption is a Google Cloud utility function that encrypts data as it is passed between buckets. The code is placed inside of a Google Cloud Function so that whenever anything is put into the specific bucket the Cloud Function applies to, that data is encrypted or deidentified with whatever method the user has selected. Bucket to Bucket Encryption works with Google Cloud Key Management Service (KMS), Google Cloud Build, and Data Loss Prevention (DLP) APIs. 

The below diagram shows how the Google Cloud function works. The user transfers files from another Google Cloud Platform project, or another Cloud Service Provider, to Google Cloud Storage. This triggers the Google Cloud Function, which ensures the user has access to the DLP and KMS APIs. The data is then deidentified or encrypted based on user input and returned to Google Cloud Storage.
 
![Diagram of Dataflow](/images/diagram.png)
