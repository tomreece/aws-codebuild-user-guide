# Create a Report Group \(Console\)<a name="test-report-group-create-console"></a>


|  | 
| --- |
| The test reporting feature is in preview release for CodeBuild and is subject to change\. | 

**To create a test report using the AWS CodeBuild console**

1. Open the AWS CodeBuild console at [https://console\.aws\.amazon\.com/codesuite/codebuild/home](https://console.aws.amazon.com/codesuite/codebuild/home)\.

1.  In the navigation pane, choose **Report groups**\. 

1. Choose **Create report group**\. 

1. For **Report group name**, enter a name for your report group\. 

1.  If you want to upload the raw data of your test report results to an S3 bucket: 

   1. Select **Backup to Amazon S3**\. 

   1. For **S3 bucket name**, enter the name of the S3 bucket\. 

   1. For **Path prefix**, enter the path in your S3 bucket where you want to upload your test results\. 

   1.  Select **Compress test result data in a zip file** to compress your raw test result data files\. 

   1.  Expand **Additional configuration** to display encryption options\. Choose one of the following: 
      +  **Default AWS managed key** to use a customer master key \(CMK\) for Amazon S3 that is managed by the AWS Key Management Service\. In CodeBuild, the default CMK is for Amazon S3 and uses the format `aws/S3`\. For more information, see [Customer Managed CMKs](https://docs.aws.amazon.com/kms/latest/developerguide/concepts.html#customer-cmk) in the *AWS Key Management Service User Guide*\. This is the default encryption option\.
      +  **Choose a custom key** to use a CMK that you create and configure\. For **AWS KMS encryption key**, enter the ARN of your encryption key\. Its format is ` arn:aws:kms:region-id:aws-account-id:key/key-id`\. For more information, see [Creating KMS Keys](https://docs.aws.amazon.com/kms/latest/developerguide/create-keys.html) in the *AWS Key Management Service User Guide*\. 
      +  **Disable artifact encryption** to disable encryption\. You might choose this if you want to share your test results, or publish them to a static website\. \(A dynamic website can run code to decrypt test results\.\)

       For more information about encryption of data at\-rest, see [Data Encryption](security-encryption.md)\. 

1. Choose **Create report group**\.