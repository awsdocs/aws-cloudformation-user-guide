# Importing existing resources into a stack<a name="resource-import-existing-stack"></a>

During this import operation, you need to provide the following\.
+ A template that describes the entire stack, including both the resources that are already part of the stack and the resources to import\. Each resource to import must have a [DeletionPolicy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-attribute-deletionpolicy.html) attribute in your template\.
+ A unique identifier for each target resource\. Visit the appropriate service console to obtain unique identifiers\.

In this walkthrough, we provide the following example template, called `templateToImport.json`\. `ServiceTable` is currently part of the stack, and `GamesTable` is the target of the import\.

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

## Import an existing resource into a stack using the AWS CloudFormation console<a name="resource-import-existing-stack-console"></a>

1. Open the AWS CloudFormation console\.

1. On the **Stacks** page, choose the stack you want to import resources into\.

1. Choose **Stack actions**, and then choose **Import resources into stack**\.  
![\[The Import resources into stack option in the console.\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/stack-actions-import.png)

1. Review the **Import overview** page, and then choose **Next**\.

1. On the **Specify template** page, provide your updated template using one of the following methods, and then choose **Next**\.
   + Choose **Amazon S3 URL**, and then specify the URL for your template in the text box\.
   + Choose **Upload a template file**, and then browse for your template\.

1. On the **Identify resources** page, identify each target resource\.

   1. Under **Identifier property**, choose the type of resource identifier\. For example, the `AWS::DynamoDB::Table` resource can be identified using the `TableName` property\.

   1. Under **Identifier value**, type the actual property value\. For example, the `TableName` for the `GamesTable` resource in the example template is `Games`\.  
![\[The Identify resources page in the console.\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/resources-to-import-identifiers.png)

   1. Choose **Next**\.

1. On the **Specify stack details** page, update any parameters, and then choose **Next**\. This automatically creates a change set\.
**Note**  
The import operation fails if you modify existing parameters that trigger a create, update, or delete operation\.

1. On the **Review *stack\-name*** page, review the resources to import, and then choose **Import resources**\. This automatically executes the change set created in the last step\. Any [stack\-level tags](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/cfn-console-add-tags.html) are applied to imported resources at this time\.

   The **Events** page for the stack displays\.   
![\[The Events tab in the console.\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/import-events.png)

1. \(Optional\) Run drift detection on the stack to make sure the template and actual configuration of the imported resources match\. For more information about detecting drift, see [Detect drift on an entire CloudFormation stack](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/detect-drift-stack.html)\.

1. \(Optional\) If your imported resources don't match their expected template configurations, either correct the template configurations or update the resources directly\. For more information about importing drifted resources, see [Resolve drift with an import operation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/resource-import-resolve-drift.html)\.

## Import an existing resource into a stack using the AWS CLI<a name="resource-import-existing-stack-cli"></a>

1. Optionally run `GetTemplateSummary` to learn which properties identify each resource type in the template\. For example, the `AWS::DynamoDB::Table` resource can be identified using the `TableName` property\. For the `GamesTable` resource in the example template, the value of `TableName` is `Games`\.

   ```
   > aws cloudformation get-template-summary 
       --template-body file://templateToImport.json
   ```

1. Compose a list of resources to import and their unique identifiers in the following format\.

   "\[\{\\"ResourceType\\":\\"*AWS::DynamoDB::Table*\\",\\"LogicalResourceId\\":\\"*GamesTable*\\",\\"ResourceIdentifier\\":\{\\"*TableName*\\":\\"*Games*\\"\}\}\]"

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

1. Review the change set to make sure the correct resources will be imported\.

   ```
   > aws cloudformation describe-change-set --change-set-name ImportChangeSet --stack-name TargetStack
   ```

1. Execute the change set to import the resources\. Any [stack\-level tags](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/cfn-console-add-tags.html) are applied to imported resources at this time\. On successful completion of the operation `(IMPORT_COMPLETE)`, the resources are successfully imported\.

   ```
   > aws cloudformation execute-change-set --change-set-name ImportChangeSet --stack-name TargetStack
   ```

1. \(Optional\) Run drift detection on the `IMPORT_COMPLETE` stack to make sure the template and actual configuration of the imported resources match\. For more information about detecting drift, see [Detect drift on an entire CloudFormation stack](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/detect-drift-stack.html)\. 

   ```
   > aws cloudformation detect-stack-drift --stack-name TargetStack
   { "Stack-Drift-Detection-Id" : "624af370-311a-11e8-b6b7-500cexample" }
   
   > aws cloudformation describe-stack-drift-detection-status --stack-drift-detection-id 624af370-311a-11e8-b6b7-500cexample
               
   > aws cloudformation describe-stack-resource-drifts --stack-name TargetStack
   ```

1. \(Optional\) If your imported resources don't match their expected template configurations, either correct the template configurations or update the resources directly\. For more information about importing drifted resources, see [Resolve drift with an import operation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/resource-import-resolve-drift.html)\.