# Resolve drift with an import operation<a name="resource-import-resolve-drift"></a>

There may be cases where a resource’s configuration has drifted from its intended configuration and you want to accept the new configuration as the intended configuration\. In most cases, you would resolve the drift results by updating the resource definition in the stack template with a new configuration and then perform a stack update\. However, if the new configuration updates a resource property that requires replacement, then the resource will be recreated during the stack update\. If you want to retain the existing resource, you can use the resource import feature to update the resource and resolve the drift results without causing the resource to be replaced\.

Resolving drift for a resource through an import operation consists of the following basic steps:
+ [Add a DeletionPolicy attribute, set to Retain, to the resource](#step_01_update_stack)\. This ensures the existing resource is retained rather than deleted when it is removed from the stack\.
+ [Remove the resource from the template and run a stack update operation](#step_02_remove_drift)\. This removes the resource from the stack, but does not delete it\.
+ [Describe the resource’s actual state in the stack template, and then import the existing resource back into the stack](#step_03_update_template)\. This adds the resource back into the stack and resolves the property differences that were causing the drift results\.

For more information on resource import, see [Bringing existing resources into CloudFormation management](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/resource-import.html)\. For a list of resources that support import, see [Resources that support import operations](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/resource-import-supported-resources.html)\.

In this example, we use the following template, named `templateToImport.json`\. 

------
#### [ Example JSON ]

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
              "BillingMode": "PROVISIONED",
              "ProvisionedThroughput":{
                 "ReadCapacityUnits":5,
                 "WriteCapacityUnits":1
              }
           }
        },
        "GamesTable": {
            "Type": "AWS::DynamoDB::Table",
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
                "BillingMode": "PROVISIONED",
                "ProvisionedThroughput": {
                    "ReadCapacityUnits": 5,
                    "WriteCapacityUnits": 1
                }
            }
        }
    }
}
```

------
#### [ Example YAML ]

```
AWSTemplateFormatVersion: 2010-09-09
Description: Import test
Resources:
  ServiceTable:
    Type: 'AWS::DynamoDB::Table'
    Properties:
      TableName: Service
      AttributeDefinitions:
        - AttributeName: key
          AttributeType: S
      KeySchema:
        - AttributeName: key
          KeyType: HASH
      BillingMode: PROVISIONED
      ProvisionedThroughput:
        ReadCapacityUnits: 5
        WriteCapacityUnits: 1
  GamesTable:
    Type: 'AWS::DynamoDB::Table'
    Properties:
      TableName: Games
      AttributeDefinitions:
        - AttributeName: key
          AttributeType: S
      KeySchema:
        - AttributeName: key
          KeyType: HASH
      BillingMode: PROVISIONED
      ProvisionedThroughput:
        ReadCapacityUnits: 5
        WriteCapacityUnits: 1
```

------

In this example, let's assume a user changed a resource *outside* of CloudFormation\. After running drift detect, we discovered that `GamesTable` has been modified `BillingMode` to `PAY_PER_REQUEST`\. For more information about drift detect, see [Detecting unmanaged configuration changes to stacks and resources](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-stack-drift.html)\.

![\[The drift results display the expected and actual results in the console.\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/drift-results-gamestable.png)

Our stack is now out of date, our resources are live, but we want to preserve the intended resource configuration\. We can do this by resolving drift through an import operation, without interrupting services\.

## Resolve drift with an import operation using the AWS CloudFormation console<a name="w7739ab1c23c19c19c24"></a>

### Step 1\. Update stack with Retain deletion policy<a name="w7739ab1c23c19c19c24b3"></a>

**To update stack using a `DeletionPolicy` attribute with the `Retain` option**

1. Sign in to the AWS Management Console and open the AWS CloudFormation console at [https://console\.aws\.amazon\.com/cloudformation](https://console.aws.amazon.com/cloudformation/)\.

1. On the **Stacks** page, choose the stack that has drifted\.

1. Choose **Update**, and then choose **Replace current template** from the stack details pane\.

1. On the **Specify template** page, provide your updated template that contains the `DeletionPolicy` attribute with the `Retain` option using one of the following methods:
   + Choose **Amazon S3 URL**, and then specify the URL for your template in the text box\.
   + Choose **Upload a template file**, and then browse for your template\.

   Then, choose **Next**\.

1. Review the **Specify stack details** page and choose **Next**\.

1. Review the **Configure stack options** page and choose **Next**\.

1. On the **Review *stack\-name*** page, choose **Update stack**\.

*Results*: On the **Events** page of your stack, the status is `UPDATE_COMPLETE`\.

To resolve drift through an import operation, without interrupting services, specify a `Retain` [DeletionPolicy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-attribute-deletionpolicy.html) for the resources you want to remove from your stack\. In the following example, we’ve added a [DeletionPolicy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-attribute-deletionpolicy.html) attribute, set to `Retain`, to the `GamesTable` resource\.

------
#### [ Example JSON ]

```
    "GamesTable": {
        "Type": "AWS::DynamoDB::Table",
        "DeletionPolicy": "Retain",
        "Properties": {
            "TableName": "Games",
```

------
#### [ Example YAML ]

```
  GamesTable:
    Type: 'AWS::DynamoDB::Table'
   DeletionPolicy: Retain
    Properties:
      TableName: Games
```

------

### Step 2\. Remove drifted resources, related parameters, and outputs<a name="w7739ab1c23c19c19c24b5"></a>

**To remove drifted resources, related parameters, and outputs**

1. Choose **Update**, and then choose **Replace current template** from the stack details pane\.

1. On the **Specify template** page, provide your updated template with its resources, related parameters, and outputs removed from the stack template using one of the following methods:
   + Choose **Amazon S3 URL**, and then specify the URL for your template in the text box\.
   + Choose **Upload a template file**, and then browse for your template\.

   Then, choose **Next**\.

1. Review the **Specify stack details** page and choose **Next**\.

1. Review the **Configure stack options** page and choose **Next**\.

1. On the **Review *stack\-name*** page, choose **Update stack**\.

*Results*: The **Logical ID** `GamesTable` has a status of `DELETE_SKIPPED` on the **Events** page of your stack\.

Wait until CloudFormation completes the stack update operation\. After the stack update operation completes, remove the resource, related parameters, and outputs from the stack template\. Then, import the updated template\. After completing these actions, the example template now looks like the following\.

------
#### [ Example JSON ]

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
              "BillingMode": "PROVISIONED",
              "ProvisionedThroughput":{
                 "ReadCapacityUnits":5,
                 "WriteCapacityUnits":1
              }
           }
        }
    }
}
```

------
#### [ Example YAML ]

```
AWSTemplateFormatVersion: 2010-09-09
Description: Import test
Resources:
  ServiceTable:
    Type: 'AWS::DynamoDB::Table'
    Properties:
      TableName: Service
      AttributeDefinitions:
        - AttributeName: key
          AttributeType: S
      KeySchema:
        - AttributeName: key
          KeyType: HASH
      BillingMode: PROVISIONED
      ProvisionedThroughput:
        ReadCapacityUnits: 5
        WriteCapacityUnits: 1
```

------

### Step 3\. Update template to match the live state of your resources<a name="w7739ab1c23c19c19c24b7"></a>

**To update template to match the live state of resources**

1. To import the updated template, choose **Stack actions** and then choose **Import resources into stack**\.  
![\[The Import resources into stack option in the console.\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/stack-actions-import.png)

1. Review the **Import overview** page for a list of things you're required to provide during this operation, and then choose **Next**\.

1. On the **Specify template** page, provide your updated template using one of the following methods:
   + Choose **Amazon S3 URL**, and then specify the URL for your template in the text box\.
   + Choose **Upload a template file**, and then browse for your template\.

   Then, choose **Next**\.

1. On the **Identify resources** page, identify each target resource\.

   1. Under **Identifier property**, choose the type of resource identifier\. For example, the `TableName` property identifies the `AWS::DynamoDB::Table` resource\.

   1. Under **Identifier value**, enter the actual property value\. In the example template, the `TableName` for the `GamesTable` resource is `Games`\.  
![\[The Identify resources page in the console.\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/resources-to-import-identifiers.png)

   1. Choose **Next**\.

1. Review the **Specify stack details** page, and choose **Next**\.

1. On the **Import overview** page, review the resources being imported, and then choose **Import resources**\. This will import the `AWS::DynamoDB::Table` resource type back into your stack\.

*Results*: In this example, we resolved the resource drift through an import operation, without interrupting services\. You can check the progress of an import action in the AWS CloudFormation console in the Events tab\. Imported resources will have a `IMPORT_COMPLETE` status followed by a `CREATE_COMPLETE` status with **Resource import complete** as the status reason\. In this example, we resolved the resource drift through an import operation, without interrupting services\.

Wait until CloudFormation completes the stack update operation\. After the stack update operation completes, update your template to match the actual, drifted state of your resources\. For example, the `BillingMode` will be set to `PAY_PER_REQUEST` and `ReadCapacityUnits` and `WriteCapacityUnits` will be set to `0`\.

------
#### [ Example JSON ]

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
              "BillingMode": "PROVISIONED",
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
                "BillingMode": "PAY_PER_REQUEST",
                "ProvisionedThroughput": {
                    "ReadCapacityUnits": 0,
                    "WriteCapacityUnits": 0
                }
            }
        }
    }
}
```

------
#### [ Example YAML ]

```
AWSTemplateFormatVersion: 2010-09-09
Description: Import test
Resources:
  ServiceTable:
    Type: 'AWS::DynamoDB::Table'
    Properties:
      TableName: Service
      AttributeDefinitions:
        - AttributeName: key
          AttributeType: S
      KeySchema:
        - AttributeName: key
          KeyType: HASH
      BillingMode: PROVISIONED
      ProvisionedThroughput:
        ReadCapacityUnits: 5
        WriteCapacityUnits: 1
  GamesTable:
    Type: 'AWS::DynamoDB::Table'
    DeletionPolicy: Retain
    Properties:
      TableName: Games
      AttributeDefinitions:
        - AttributeName: key
          AttributeType: S
      KeySchema:
        - AttributeName: key
          KeyType: HASH
      BillingMode: PAY_PER_REQUEST
      ProvisionedThroughput:
        ReadCapacityUnits: 0
        WriteCapacityUnits: 0
```

------