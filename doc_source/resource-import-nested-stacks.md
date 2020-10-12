# Nesting an existing stack<a name="resource-import-nested-stacks"></a>

Use the `resource import` feature to nest an existing stack within another existing stack\. Nested stacks are common components that you declare and reference from within other templates\. That way, you can avoid copying and pasting the same configurations into your templates and simplify stack updates\. If you have a template for a common component, you can use the `AWS::CloudFormation::Stack` resource to reference this template from within another template\. For more information on nested stacks, see [Working with nested stacks](using-cfn-nested-stacks.md)\.

AWS CloudFormation only supports one level of nesting using `resource import`\. This means that you cannot import a stack into a child stack or import a stack that has children\.

## Nested stack import validation<a name="resource-import-nested-stacks-validation"></a>

During a nested stack import operation, AWS CloudFormation performs the following validations\.
+ The nested `AWS::CloudFormation::Stack` definition in the parent stack template matches the actual nested stack's template\.
+ The tags for the nested `AWS::CloudFormation::Stack` definition in the parent stack template match the tags for the actual nested stack resource\.

## Nest an existing stack using the AWS Management Console<a name="resource-import-nested-stacks-console"></a>

1. Add the `AWS::CloudFormation::Stack` resource to the parent stack template with a `Retain` [DeletionPolicy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-attribute-deletionpolicy.html)\. In the following example parent template, `NestedStack` is the target of the import\.

   ```
   {
     "AWSTemplateFormatVersion" : "2010-09-09",
     "Resources" : {
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
       "NestedStack" : {
         "Type" : "AWS::CloudFormation::Stack",
         "DeletionPolicy": "Retain",
         "Properties" : {
         "TemplateURL" : "https://s3.amazonaws.com/cloudformation-templates-us-east-2/EC2ChooseAMI.template",
           "Parameters" : {
             "InstanceType" : "t1.micro",
             "KeyName" : "mykey"
           }
         }
       }
     }
   }
   ```

1. Open the AWS CloudFormation console\.

1. On the **Stacks** page, with the parent stack selected, choose **Stack actions**, and then choose **Import resources into stack**\.  
![\[The Import resources into stack option in the console.\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/stack-actions-import.png)

1. Read the **Import overview** page for a list of things you're required to provide during this operation\. Then, choose **Next**\.

1. On the **Specify template** page, provide the updated parent template using one of the following methods, and then choose **Next**\.
   + Choose **Amazon S3 URL**, and then specify the URL for your template in the text box\.
   + Choose **Upload a template file**, and then browse for your template\.

1. On the **Identify resources** page, identify the `AWS::CloudFormation::Stack` resource\.

   1. Under **Identifier property**, choose the type of resource identifier\. For example, an `AWS::CloudFormation::Stack` resource can be identified using the `StackId` property\.

   1. Under **Identifier value**, type the actual property value\. For example, `arn:aws:cloudformation:us-west-2:12345678910:stack/mystack/5b918d10-cd98-11ea-90d5-0a9cd3354c10`\.  
![\[The Identify resources page in the console.\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/resource-import-stackid.png)

   1. Choose **Next**\.

1. On the **Specify stack details** page, modify any parameters, and then choose **Next**\. This automatically creates a change set\.
**Important**  
The import operation fails if you modify existing parameters that trigger a create, update, or delete operation\.

1. On the **Review *stack\-name*** page, confirm that the correct resource is being imported, and then choose **Import resources**\. This automatically executes the change set created in the last step\. Any [stack\-level tags](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/cfn-console-add-tags.html) are applied to imported resources at this time\.

1. The **Events** pane of the **Stack details** page for your parent stack displays\.  
![\[The Events tab in the console.\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/import-events.png)
**Note**  
It's not necessary to run drift detection on the parent stack after this import operation because the `AWS::CloudFormation::Stack`resource was already managed by AWS CloudFormation\.

## Nest an existing stack using the AWS CLI<a name="resource-import-nested-stacks-cli"></a>

1. Add the `AWS::CloudFormation::Stack` resource to the parent stack template with a `Retain` [DeletionPolicy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-attribute-deletionpolicy.html)\. In the following example parent template, `NestedStack` is the target of the import\.

   ```
   {
     "AWSTemplateFormatVersion" : "2010-09-09",
     "Resources" : {
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
       "NestedStack" : {
         "Type" : "AWS::CloudFormation::Stack",
         "DeletionPolicy": "Retain",
         "Properties" : {
         "TemplateURL" : "https://s3.amazonaws.com/cloudformation-templates-us-east-2/EC2ChooseAMI.template",
           "Parameters" : {
             "InstanceType" : "t1.micro",
             "KeyName" : "mykey"
           }
         }
       }
     }
   }
   ```

1. Create a change set of type `IMPORT` with the following parameters\. `--resources-to-import` does not support inline YAML\.

   ```
   > aws cloudformation create-change-set
       --stack-name TargetParentStack --change-set-name ImportChangeSet
       --change-set-type IMPORT
       --resources-to-import "[{\"ResourceType\":\AWS::CloudFormation::Stack\",\"LogicalResourceId\":\"MyStack\",\"ResourceIdentifier\":{\"StackId\":\"arn:aws:cloudformation:us-east-2:123456789012:stack/mystack-mynestedstack-sggfrhxhum7w/f449b250-b969-11e0-a185-5081d0136786\"}}]
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
         "ResourceType":"AWS::CloudFormation::Stack",
         "LogicalResourceId":"MyStack",
         "ResourceIdentifier": {
           "StackId":"arn:aws:cloudformation:us-east-2:123456789012:stack/mystack-mynestedstack-sggfrhxhum7w/f449b250-b969-11e0-a185-5081d0136786"
         }
     }
   ]
   ```

1. Review the change set to make sure the correct stack is being imported\.

   ```
   > aws cloudformation describe-change-set --change-set-name ImportChangeSet
   ```

1. Execute the change set to import stack into the source parent stack\. Any [stack\-level tags](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/cfn-console-add-tags.html) are applied to imported resources at this time\. On successful completion of the import operation `(IMPORT_COMPLETE)`, the stack is successfully nested\.

   ```
   > aws cloudformation execute-change-set --change-set-name ImportChangeSet
   ```
**Note**  
It's not necessary to run drift detection on the parent stack after this import operation because the `AWS::CloudFormation::Stack`resource was already managed by AWS CloudFormation\.