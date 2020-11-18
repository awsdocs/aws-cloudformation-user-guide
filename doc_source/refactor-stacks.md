# Moving resources between stacks<a name="refactor-stacks"></a>

Using the `resource import` feature, you can move resources between, or *refactor*, stacks\. You need to first add a `Retain` deletion policy to the resource you want to move to ensure that the resource is preserved when you remove it from the source stack and import it to the target stack\.

**Important**  
Not all resources support import operations\. See [Resources that support import operations](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/resource-import-supported-resources.html) before you remove a resource from your stack\. If you remove a resource that doesn't support import operations from your stack, you can't import the resource into another stack or bring it back into the source stack\.

## Refactor a stack using the AWS Management Console<a name="refactor-stacks-console"></a>

1. In the source template, specify a `Retain` [DeletionPolicy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-attribute-deletionpolicy.html) for the resource you want to move\.

   In the following example source template, `Games` is the target of this refactor\.  
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

   1. On the **Stacks** page, with the stack selected, choose **Update**\.

   1. Under **Prepare template**, choose **Replace current template**\.

   1. Under **Specify template**, provide the updated source template with the `DeletionPolicy` attribute on `GamesTable`, and then choose **Next**\.
      + Choose **Amazon S3 URL**, and then specify the URL to the updated source template in the text box\.
      + Choose **Upload a template file**, and then browse for the updated source template file\.

   1. On the **Specify stack details** page, no changes are required\. Choose **Next**\.

   1. On the **Configure stack options** page, no changes are required\. Choose **Next**\.

   1. On the **Review *stack\_name*** page, review your changes\. If your template contains IAM resources, select **I acknowledge that this template may create IAM resources** to specify that you want to use IAM resources in the template\. For more information about using IAM resources in templates, see [Controlling access with AWS Identity and Access Management](using-iam-template.md)\. Then, either update your source stack by creating a change set or update your source stack directly\.

1. Remove the resource, related parameters, and outputs from the source template, and then add them to the target template\.

   The source template now looks like the following\.  
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

   The following example target template currently has the `PlayersTable` resource, and now also contains `GamesTable`\.  
**Example JSON**  

   ```
   {
       "AWSTemplateFormatVersion": "2010-09-09",
       "Description": "Import test",
       "Resources": {
           "PlayersTable": {
               "Type": "AWS::DynamoDB::Table",
               "Properties": {
                   "TableName": "Players",
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

1. Repeat steps 2\-3 to update the source stack again, this time to delete the target resource from the stack\.

1. Perform an import operation to add `GamesTable` to the target stack\.

   1. On the **Stacks** page, with the parent stack selected, choose **Stack actions**, and then choose **Import resources into stack**\.  
![\[The Import resources into stack option in the console.\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/stack-actions-import.png)

   1. Read the **Import overview** page for a list of things you're required to provide during this operation\. Then, choose **Next**\.

   1. On the **Specify template** page, do one of the following, and then choose **Next**\.
      + Choose **Amazon S3 URL**, and then specify a URL in the text box\.
      + Choose **Upload a template file**, and then browse for a file to upload\.

   1. On the **Identify resources** page, identify the resource you're moving \(in this example, `GamesTable`\)\.

      1. Under **Identifier property**, choose the type of resource identifier\. For example, an `AWS::DynamoDB::Table` resource can be identified using the `TableName` property\.

      1. Under **Identifier value**, type the actual property value\. For example, `GamesTables`\.  
![\[The Identify resources page in the console.\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/resources-to-import-identifiers.png)

      1. Choose **Next**\.

   1. On the **Specify stack details** page, modify any parameters, and then choose **Next**\. This automatically creates a change set\.
**Important**  
The import operation fails if you modify existing parameters that trigger a create, update, or delete operation\.

   1. On the **Review *stack\-name*** page, confirm that the correct resource is being imported, and then choose **Import resources**\. This automatically executes the change set created in the last step\. Any [stack\-level tags](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/cfn-console-add-tags.html) are applied to imported resources at this time\.

   1. The **Events** pane of the **Stack details** page for your parent stack displays\.  
![\[The Events tab in the console.\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/import-events.png)
**Note**  
It's not necessary to run drift detection on the parent stack after this import operation because the `AWS::CloudFormation::Stack` resource is already managed by AWS CloudFormation\.

## Refactor a stack using the AWS CLI<a name="refactor-stacks-cli"></a>

1. In the source template, specify a `Retain` [DeletionPolicy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-attribute-deletionpolicy.html) for the resource you want to move\.

   In the following example source template, `GamesTable` is the target of this refactor\.  
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

1. Update the source stack to apply the deletion policy to the resource\.

   ```
   update-stack --stack-name "source-stack-name"
   ```

1. Remove the resource, related parameters, and outputs from the source template, and then add them to the target template\.

   The source template now looks like the following\.  
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

   The following example target template currently has the `PlayersTable` resource, and now also contains `GamesTable`\.  
**Example JSON**  

   ```
   {
       "AWSTemplateFormatVersion": "2010-09-09",
       "Description": "Import test",
       "Resources": {
           "PlayersTable": {
               "Type": "AWS::DynamoDB::Table",
               "Properties": {
                   "TableName": "Players",
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

1. Update the source stack to delete the `GamesTable` resource and its related parameters and outputs from the stack\.

   ```
   aws cloudformation update-stack --stack-name "source-stack-name"
   ```

1. Create a change set of type `IMPORT` with the following parameters\. `--resources-to-import` does not support inline YAML\.

   ```
   > aws cloudformation create-change-set
       --stack-name TargetStack --change-set-name ImportChangeSet
       --change-set-type IMPORT
       --resources-to-import "[{\"ResourceType\":\"AWS::DynamoDB::Table\",\"LogicalResourceId\":\"GamesTable\",\"ResourceIdentifier\":{\"TableName\":\"Games\"}}]"
       --template-body file://templateToImport.json
   ```

   The AWS CLI also supports text files as input for the `resources-to-import` parameter, as shown in the following example\. 

   ```
   --resources-to-import: file://resourcesToImport.txt
   ```

   In this walkthrough, *file://resourcesToImport\.txt* contains the following\.

   ```
   [
     {
         "ResourceType":"AWS::DynamoDB::Table",
         "LogicalResourceId":"GamesTable",
         "ResourceIdentifier": {
           "TableName":"Games"
         }
     }
   ]
   ```

1. Review the change set to make sure the correct resource is being imported into the target stack\.

   ```
   > aws cloudformation describe-change-set --change-set-name ImportChangeSet
   ```

1. Execute the change set to import the resource into the target stack\. Any [stack\-level tags](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/cfn-console-add-tags.html) are applied to imported resources at this time\. On successful completion of the operation `(IMPORT_COMPLETE)`, the resource is successfully imported\.

   ```
   > aws cloudformation execute-change-set --change-set-name ImportChangeSet
   ```
**Note**  
It's not necessary to run drift detection on the target stack after this import operation because the resource is already managed by AWS CloudFormation\.