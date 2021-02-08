# Creating a stack from existing resources<a name="resource-import-new-stack"></a>

During this import operation, you need to provide the following\.
+ A template that describes the resources that will be in the new stack and the resource configurations\. Each resource in your template must have a [DeletionPolicy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-attribute-deletionpolicy.html) attribute\.
+ A unique identifier for each target resource\. Visit the appropriate service console to obtain unique identifiers\.

In this walkthrough, we provide the following example template, called `templateToImport.json`\. `ServiceTable` and `GamesTable` are the targets of the import\.

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Description": "Import test",
    "Resources": {
         "ServiceTable":{
           "Type":"AWS::DynamoDB::Table",
           "DeletionPolicy": "Retain",
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

## Create a stack from existing resources using the AWS CloudFormation console<a name="resource-import-new-stack-console"></a>

1. Open the AWS CloudFormation console\.

1. On the **Stacks** page, choose **Create stack**, and then choose **With existing resources \(import resources\)**\.  
![\[The Create stack from existing resources option in the console.\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/create-stack-with-existing-resources.png)

1. Read the **Import overview** page for a list of things you're required to provide during this operation\. Then, choose **Next**\.

1. On the **Specify template** page, provide your template using one of the following methods, and then choose **Next**\.
   + Choose **Amazon S3 URL**, and then specify the URL for your template in the text box\.
   + Choose **Upload a template file**, and then browse for your template\.

1. On the **Identify resources** page, identify each target resource\.

   1. Under **Identifier property**, choose the type of resource identifier\. For example, the `AWS::DynamoDB::Table` resource can be identified using the `TableName` property\.

   1. Under **Identifier value**, type the actual property value\. For example, the `TableName` for the `GamesTable` resource in the example template is `Games`\.  
![\[The Identify resources page in the console.\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/resources-to-import-identifiers.png)

   1. Choose **Next**\.

1. On the **Specify stack details** page, modify any parameters, and then choose **Next**\. This automatically creates a change set\.
**Important**  
The import operation fails if you modify existing parameters that trigger a create, update, or delete operation\.

1. On the **Review *stack\-name*** page, confirm that the correct resources are being imported, and then choose **Import resources**\. This automatically executes the change set created in the last step\.

   The **Events** pane of the **Stack details** page for your new stack displays\.  
![\[The Events tab in the console.\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/import-events.png)

1. \(Optional\) Run drift detection on the stack to make sure the template and actual configuration of the imported resources match\. For more information about detecting drift, see [Detect drift on an entire CloudFormation stack](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/detect-drift-stack.html)\. 

1. \(Optional\) If your imported resources don't match their expected template configurations, either correct the template configurations or update the resources directly\. In this walkthrough, we correct the template configurations to match their actual configurations\.

   1. [Revert the import operation](resource-import-revert.md#resource-import-revert-console) for the affected resources\.

   1. Add the import targets to your template again, making sure that the template configurations match the actual configurations\.

   1. Repeat steps 2\-8 using the modified template to import the resources again\.

## Create a stack from existing resources using the AWS CLI<a name="resource-import-new-stack-cli"></a>

1. Open the AWS CLI\.

1. Optionally run `GetTemplateSummary` to learn which properties identify each resource type in your template\. For example, the `AWS::DynamoDB::Table` resource can be identified using the `TableName` property\. For the `GamesTable` resource in the example template, the value of `TableName` is `Games`\.

   ```
   > aws cloudformation get-template-summary
       --template-body file://templateToImport.json
   ```

1. Compose a list of the target resources from your template and their unique identifiers in the following format\.

   "\[\{\\"ResourceType\\":\\"*AWS::DynamoDB::Table*\\",\\"LogicalResourceId\\":\\"*GamesTable*\\",\\"ResourceIdentifier\\":\{\\"*TableName*\\":\\"*Games*\\"\}\}\]"

1. Create a change set of type `IMPORT` with the following parameters\. `--resources-to-import` does not support inline YAML\.

   ```
   > aws cloudformation create-change-set
       --stack-name TargetStack --change-set-name ImportChangeSet
       --change-set-type IMPORT
       --resources-to-import "[{\"ResourceType\":\"AWS::DynamoDB::Table\",\"LogicalResourceId\":\"GamesTable\",\"ResourceIdentifier\":{\"TableName\":\"Games\"}},{\"ResourceType\":\"AWS::DynamoDB::Table\",\"LogicalResourceId\":\"ServiceTable\",\"ResourceIdentifier\":{\"TableName\":\"Service\"}}]"
       --template-body file://templateToImport.json
   ```

   The AWS CLI also supports text files as input for the `--resources-to-import` parameter, as shown in the following example\.

   ```
   --resources-to-import file://resourcesToImport.txt
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
     },
     {
         "ResourceType":"AWS::DynamoDB::Table",
         "LogicalResourceId":"ServiceTable",
         "ResourceIdentifier": {
           "TableName":"Service"
         }
     }
   ]
   ```

1. Review the change set to make sure the correct resources will be imported\.

   ```
   > aws cloudformation describe-change-set --change-set-name ImportChangeSet --stack-name TargetStack
   ```

1. Execute the change set to import the resources\. On successful completion of the operation `(IMPORT_COMPLETE)`, the resources are successfully imported\.

   ```
   > aws cloudformation execute-change-set --change-set-name ImportChangeSet --stack-name TargetStack
   ```

1. \(Optional\) Run drift detection on the `IMPORT_COMPLETE` stack to make sure the template and actual configuration of the imported resources match\. For more information on detecting drift, see [Detect drift on an entire CloudFormation stack](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/detect-drift-stack.html)\.

   ```
   > aws cloudformation detect-stack-drift --stack-name TargetStack
   { "Stack-Drift-Detection-Id" : "624af370-311a-11e8-b6b7-500cexample" }
   
   > aws cloudformation describe-stack-drift-detection-status --stack-drift-detection-id 624af370-311a-11e8-b6b7-500cexample
               
   > aws cloudformation describe-stack-resource-drifts --stack-name TargetStack
   ```

1. \(Optional\) If your imported resources don't match their expected template configurations, either correct the template configurations or update the resources directly\. In this walkthrough, we correct the template configurations to match their actual configurations\.

   1. [Revert the import operation](resource-import-revert.md#resource-import-revert-cli) for the affected resources\.

   1. Add the import targets to your template again, making sure that the template configurations match the actual configurations\.

   1. Repeat steps 4\-7 using the modified template to import the resources again\.