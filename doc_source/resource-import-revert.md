# Reverting an import operation<a name="resource-import-revert"></a>

To revert an import operation, specify a `Retain` deletion policy for the resource you want to remove from the template to ensure that it's preserved when you delete it from the stack\.

## Revert an import operation using the AWS Management Console<a name="resource-import-revert-console"></a>

1. Specify a `Retain` [DeletionPolicy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-attribute-deletionpolicy.html) for the resources you want to remove from your stack\. In the following example template, `GamesTable` is the target of this revert operation\.  
**Example JSON**  

   ```
   {
       "AWSTemplateFormatVersion": "2010-09-09",
       "Description": "Import test",
       "Resources": {
           "ServiceTable":{
              "Type":"AWS::DynamoDB::Table",
              "Properties":{
                 "TableName":"Service",
                 "AttributeDefinitions":[
                    {
                       "AttributeName":"key",
                       "AttributeType":"S"
                    }
                 ],
                 "KeySchema":[
                    {
                       "AttributeName":"key",
                       "KeyType":"HASH"
                    }
                 ],
                 "ProvisionedThroughput":{
                    "ReadCapacityUnits":5,
                    "WriteCapacityUnits":1
                 }
              }
           },
           "GamesTable": {
               "Type": "AWS::DynamoDB::Table",
               "DeletionPolicy": "Retain",
               "Properties": {
                   "TableName": "Games",
                   "AttributeDefinitions": [
                       {
                           "AttributeName": "key",
                           "AttributeType": "S"
                       }
                   ],
                   "KeySchema": [
                       {
                           "AttributeName": "key",
                           "KeyType": "HASH"
                       }
                   ],
                   "ProvisionedThroughput": {
                       "ReadCapacityUnits": 5,
                       "WriteCapacityUnits": 1
                   }
               }
           }
       }
   }
   ```

1. Open the AWS CloudFormation console to perform a stack update to apply the deletion policy\.

   1. On the **Stacks** page, with the stack selected, choose **Update**, and then choose **Update stack \(standard\)**\.

   1. Under **Prepare template**, choose **Replace current template**\.

   1. Under **Specify template**, provide the updated source template with the `DeletionPolicy` attribute on `GamesTable`, and then choose **Next**\.
      + Choose **Amazon S3 URL**, and then specify the URL to the updated source template in the text box\.
      + Choose **Upload a template file**, and then browse for the updated source template file\.

   1. On the **Specify stack details** page, no changes are required\. Choose **Next**\.

   1. On the **Configure stack options** page, no changes are required\. Choose **Next**\.

   1. On the **Review *stack\_name*** page, review your changes\. If your template contains IAM resources, select **I acknowledge that this template may create IAM resources** to specify that you want to use IAM resources in the template\. For more information about using IAM resources in templates, see [Controlling access with AWS Identity and Access Management](using-iam-template.md)\. Then, either update your source stack by creating a change set or update your source stack directly\.

1. Remove the resource, related parameters, and outputs from the stack template\. In this example, the template now looks like the following\.  
**Example JSON**  

   ```
   {
       "AWSTemplateFormatVersion": "2010-09-09",
       "Description": "Import test",
       "Resources": {
           "ServiceTable":{
              "Type":"AWS::DynamoDB::Table",
              "Properties":{
                 "TableName":"Service",
                 "AttributeDefinitions":[
                    {
                       "AttributeName":"key",
                       "AttributeType":"S"
                    }
                 ],
                 "KeySchema":[
                    {
                       "AttributeName":"key",
                       "KeyType":"HASH"
                    }
                 ],
                 "ProvisionedThroughput":{
                    "ReadCapacityUnits":5,
                    "WriteCapacityUnits":1
                 }
              }
           }
       }
   }
   ```

1. Repeat step 2 to delete the resource \(`GamesTable`\) and its related parameters and outputs from the stack\.

## Revert an import operation using the AWS CLI<a name="resource-import-revert-cli"></a>

1. Specify a `Retain` [DeletionPolicy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-attribute-deletionpolicy.html) for the resources you want to remove from your stack\. In the following example template, `GamesTable` is the target of this revert operation\.  
**Example JSON**  

   ```
   {
       "AWSTemplateFormatVersion": "2010-09-09",
       "Description": "Import test",
       "Resources": {
           "ServiceTable":{
              "Type":"AWS::DynamoDB::Table",
              "Properties":{
                 "TableName":"Service",
                 "AttributeDefinitions":[
                    {
                       "AttributeName":"key",
                       "AttributeType":"S"
                    }
                 ],
                 "KeySchema":[
                    {
                       "AttributeName":"key",
                       "KeyType":"HASH"
                    }
                 ],
                 "ProvisionedThroughput":{
                    "ReadCapacityUnits":5,
                    "WriteCapacityUnits":1
                 }
              }
           },
           "GamesTable": {
               "Type": "AWS::DynamoDB::Table",
               "DeletionPolicy": "Retain",
               "Properties": {
                   "TableName": "Games",
                   "AttributeDefinitions": [
                       {
                           "AttributeName": "key",
                           "AttributeType": "S"
                       }
                   ],
                   "KeySchema": [
                       {
                           "AttributeName": "key",
                           "KeyType": "HASH"
                       }
                   ],
                   "ProvisionedThroughput": {
                       "ReadCapacityUnits": 5,
                       "WriteCapacityUnits": 1
                   }
               }
           }
       }
   }
   ```

1. Update the stack to apply the deletion policy to the resource\.

   ```
   update-stack --stack-name "stack-name"
   ```

1. Remove the resource, related parameters, and outputs from the stack template\. In this example, the template now looks like the following\.  
**Example JSON**  

   ```
   {
       "AWSTemplateFormatVersion": "2010-09-09",
       "Description": "Import test",
       "Resources": {
           "ServiceTable":{
              "Type":"AWS::DynamoDB::Table",
              "Properties":{
                 "TableName":"Service",
                 "AttributeDefinitions":[
                    {
                       "AttributeName":"key",
                       "AttributeType":"S"
                    }
                 ],
                 "KeySchema":[
                    {
                       "AttributeName":"key",
                       "KeyType":"HASH"
                    }
                 ],
                 "ProvisionedThroughput":{
                    "ReadCapacityUnits":5,
                    "WriteCapacityUnits":1
                 }
              }
           }
       }
   }
   ```

1. Update the stack to delete the resource \(`GamesTable`\) and its related parameters and outputs from the stack\.

   ```
   update-stack --stack-name "stack-name"
   ```