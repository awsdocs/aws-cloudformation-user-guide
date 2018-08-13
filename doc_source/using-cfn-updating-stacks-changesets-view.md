# Viewing a Change Set<a name="using-cfn-updating-stacks-changesets-view"></a>

After you create a change set, you can view the proposed changes before executing them\. You can use the AWS CloudFormation console, AWS CLI, or AWS CloudFormation API to view change sets\. The AWS CloudFormation console provides a summary of the changes and a detailed list of changes in JSON format\. The AWS CLI and AWS CloudFormation API return a detailed list of changes in JSON format\.

**To view a change \(console\)**

1. In the AWS CloudFormation console, choose the stack that has the change set that you want to view\.

1. In the stack detail pane, choose **Change Sets** to view a list of the stack's change sets\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/console-changeset-tab.png)

1. Choose the change set that you want view\.

   The AWS CloudFormation console directs you to the change set's detail page, where you can see the time the change set was created, its status, the input used to generate the change set, and a summary of changes\.

   In the **Changes** section, each line represents a resource that AWS CloudFormation will add, delete, or modify\. AWS CloudFormation adds a resource when you add a resource to the stack's template\. AWS CloudFormation deletes a resource when you delete an existing resource from the stack's template\. AWS CloudFormation modifies a resource when you change the properties of a resource\. Note that a modification can cause the resource to be interrupted or replaced \(recreated\)\. For more information about resource update behaviors, see [Update Behaviors of Stack Resources](using-cfn-updating-stacks-update-behaviors.md)\.

   To focus on specific changes, use the filter view\. For example, filter for a specific resource type, such as **AWS::EC2::Instance**\. To filter for a specific resource, specify its logical or physical ID, such as **myWebServer** or **i\-123abcd4**\.

   If you want to consider other changes before you decide which changes to make, create additional change sets\.

**To view a change set \(AWS CLI\)**

1. To get the ID of the change set, run the [aws cloudformation list\-change\-sets](http://docs.aws.amazon.com/cli/latest/reference/cloudformation/list-change-sets.html) command\.

   Specify the stack ID of the stack that has the change set that you want to view, as shown in the following example:

   ```
   aws cloudformation list-change-sets --stack-name arn:aws:cloudformation:us-east-1:123456789012:stack/SampleStack/1a2345b6-0000-00a0-a123-00abc0abc000
   ```

   AWS CloudFormation returns a list of change sets, similar to the following:

   ```
   {
       "Summaries": [
           {
               "StackId": "arn:aws:cloudformation:us-east-1:123456789012:stack/SampleStack/1a2345b6-0000-00a0-a123-00abc0abc000",
               "Status": "CREATE_COMPLETE",
               "ChangeSetName": "SampleChangeSet",
               "CreationTime": "2016-03-16T20:44:05.889Z",
               "StackName": "SampleStack",
               "ChangeSetId": "arn:aws:cloudformation:us-east-1:123456789012:changeSet/SampleChangeSet/1a2345b6-0000-00a0-a123-00abc0abc000"
           },
           {
               "StackId": "arn:aws:cloudformation:us-east-1:123456789012:stack/SampleStack/1a2345b6-0000-00a0-a123-00abc0abc000",
               "Status": "CREATE_COMPLETE",
               "ChangeSetName": "SampleChangeSet-conditional",
               "CreationTime": "2016-03-16T21:15:56.398Z",
               "StackName": "SampleStack",
               "ChangeSetId": "arn:aws:cloudformation:us-east-1:123456789012:changeSet/SampleChangeSet-conditional/1a2345b6-0000-00a0-a123-00abc0abc000"
           },
           {
               "StackId": "arn:aws:cloudformation:us-east-1:123456789012:stack/SampleStack/1a2345b6-0000-00a0-a123-00abc0abc000",
               "Status": "CREATE_COMPLETE",
               "ChangeSetName": "SampleChangeSet-replacement",
               "CreationTime": "2016-03-16T21:03:37.706Z",
               "StackName": "SampleStack",
               "ChangeSetId": "arn:aws:cloudformation:us-east-1:123456789012:changeSet/SampleChangeSet-replacement/1a2345b6-0000-00a0-a123-00abc0abc000"
           }
       ]
   }
   ```

1. Run the [aws cloudformation describe\-change\-set](http://docs.aws.amazon.com/cli/latest/reference/cloudformation/describe-change-set.html) command, specifying the ID of the change set that you want to view\. For example:

   ```
   aws cloudformation describe-change-set --change-set-name arn:aws:cloudformation:us-east-1:123456789012:changeSet/SampleChangeSet/1a2345b6-0000-00a0-a123-00abc0abc000
   ```

   AWS CloudFormation returns information about the specified change set:

   ```
   {
       "StackId": "arn:aws:cloudformation:us-east-1:123456789012:stack/SampleStack/1a2345b6-0000-00a0-a123-00abc0abc000",
       "Status": "CREATE_COMPLETE",
       "ChangeSetName": "SampleChangeSet-direct",
       "Parameters": [
           {
               "ParameterValue": "testing",
               "ParameterKey": "Purpose"
           },
           {
               "ParameterValue": "ellioty-useast1",
               "ParameterKey": "KeyPairName"
           },
           {
               "ParameterValue": "t2.micro",
               "ParameterKey": "InstanceType"
           }
       ],
       "Changes": [
           {
               "ResourceChange": {
                   "ResourceType": "AWS::EC2::Instance",
                   "PhysicalResourceId": "i-1abc23d4",
                   "Details": [
                       {
                           "ChangeSource": "DirectModification",
                           "Evaluation": "Static",
                           "Target": {
                               "Attribute": "Tags",
                               "RequiresRecreation": "Never"
                           }
                       }
                   ],
                   "Action": "Modify",
                   "Scope": [
                       "Tags"
                   ],
                   "LogicalResourceId": "MyEC2Instance",
                   "Replacement": "False"
               },
               "Type": "Resource"
           }
       ],
       "CreationTime": "2016-03-17T23:35:25.813Z",
       "Capabilities": [],
       "StackName": "SampleStack",
       "NotificationARNs": [],
       "ChangeSetId": "arn:aws:cloudformation:us-east-1:123456789012:changeSet/SampleChangeSet-direct/9edde307-960d-4e6e-ad66-b09ea2f20255"
   }
   ```

   The `Changes` key lists changes to resources\. If you were to execute this change set, AWS CloudFormation would update the tags of the `i-1abc23d4` EC2 instance\. For a description of each field, see the [Change](http://docs.aws.amazon.com/AWSCloudFormation/latest/APIReference/API_Change.html) data type in the *AWS CloudFormation API Reference*\.

   For additional examples of change sets, see [Example Change Sets](using-cfn-updating-stacks-changesets-samples.md)\.