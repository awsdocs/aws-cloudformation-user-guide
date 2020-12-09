# Viewing a change set<a name="using-cfn-updating-stacks-changesets-view"></a>

After you create a change set, you can view the proposed changes before executing them\. You can use the AWS CloudFormation console, AWS CLI, or AWS CloudFormation API to view change sets\. The AWS CloudFormation console provides a summary of the changes and a detailed list of changes in JSON format\. The AWS CLI and AWS CloudFormation API return a detailed list of changes in JSON format\.

------
#### [ View a change set for nested stack \(console\) ]

**To view a change set for nested stacks \(console\)**

1. In the [AWS CloudFormation console](https://console.aws.amazon.com/cloudformation), in **Stacks**, choose the name of the stack that contains the change set that you want to view\.

1. In the navigation pane, choose **Change Sets** to view a list of the stack's change sets\.

1. Choose the name of the change set that you want to view\.

   The AWS CloudFormation console directs you to the change set's details page, where you can see the time the change set was created, its status, the input used to generate the change set, and a summary of the changes\.  
![\[The details page for the change set.\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/console-nested-stacks-change-sets-details.png)

   In the **Changes** section, each row represents a resource that AWS CloudFormation will add, modify, remove, or show the status of dynamic\. 
   + **Add** \- AWS CloudFormation creates a resource when you add a resource to the stack's template\.
   + **Modify** \- AWS CloudFormation modifies a resource when you change the properties of a resource in the stack's template\.
   + **Remove** \- AWS CloudFormation deletes a resource when you delete a resource from the stack's template\.
   + **Dynamic** \- AWS CloudFormation cannot determine the exact resource change action from the nested stack's template\.
**Note**  
A modification can cause the resource to be interrupted or replaced \(recreated\)\. For more information about resource update behaviors, see [Update behaviors of stack resources](using-cfn-updating-stacks-update-behaviors.md)\.

   To focus on specific changes, use the filter view\. For example, filter for a specific resource type, such as **AWS::CloudFormation::Stack**\. To filter for a specific resource, specify its logical or physical ID, such as **DeadLetterQueue** or **NestedStack**\.

1. In the **Changes** section, choose **View nested change set** of the nested change set you want to view\.

   The AWS CloudFormation console directs you to the nested change set's details page\. You can choose **Go to root change set** to view the root change set or, you can choose **View parent change set** to view the parent change set\. For more information see, [Change sets for nested stacks](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/change-sets-for-nested-stacks.html)\.  
![\[The details page for the nested change set.\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/console-nested-stacks-change-sets-details01.png)

------
#### [ View a change set \(console\) ]

**To view a change set \(console\)**

1. In the [AWS CloudFormation console](https://console.aws.amazon.com/cloudformation), in **Stacks**, choose the name of the stack that contains the change set that you want to view\.

1. In the navigation pane, choose **Change Sets** to view a list of the stack's change sets\.

1. Choose the name of the change set that you want to view\.

   The AWS CloudFormation console directs you to the change set's details page, where you can see the time the change set was created, its status, the input used to generate the change set, and a summary of the changes\.  
![\[The details page for the change set.\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/console-stacks-change-sets-details.png)

   In the **Changes** section, each row represents a resource that AWS CloudFormation will add, modify, or remove\. 
   + **Add** \- AWS CloudFormation creates a resource when you add a resource to the stack's template\.
   + **Modify** \- AWS CloudFormation modifies a resource when you change the properties of a resource in the stack's template\.
   + **Remove** \- AWS CloudFormation deletes a resource when you delete a resource from the stack's template\.
**Note**  
A modification can cause the resource to be interrupted or replaced \(recreated\)\. For more information about resource update behaviors, see [Update behaviors of stack resources](using-cfn-updating-stacks-update-behaviors.md)\.

   To focus on specific changes, use the filter view\. For example, filter for a specific resource type, such as **AWS::EC2::Instance**\. To filter for a specific resource, specify its logical or physical ID, such as **myWebServer** or **i\-123abcd4**\.

------

**To view a change set \(AWS CLI\)**

1. To get the ID of the change set, run the [aws cloudformation list\-change\-sets](https://docs.aws.amazon.com/cli/latest/reference/cloudformation/list-change-sets.html) command\.

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
               "CreationTime": "2020-11-18T20:44:05.889Z",
               "StackName": "SampleStack",
               "ChangeSetId": "arn:aws:cloudformation:us-east-1:123456789012:changeSet/SampleChangeSet/1a2345b6-0000-00a0-a123-00abc0abc000"
           },
           {
               "StackId": "arn:aws:cloudformation:us-east-1:123456789012:stack/SampleStack/1a2345b6-0000-00a0-a123-00abc0abc000",
               "Status": "CREATE_COMPLETE",
               "ChangeSetName": "SampleChangeSet-conditional",
               "CreationTime": "2020-11-18T21:15:56.398Z",
               "StackName": "SampleStack",
               "ChangeSetId": "arn:aws:cloudformation:us-east-1:123456789012:changeSet/SampleChangeSet-conditional/1a2345b6-0000-00a0-a123-00abc0abc000"
           },
           {
               "StackId": "arn:aws:cloudformation:us-east-1:123456789012:stack/SampleStack/1a2345b6-0000-00a0-a123-00abc0abc000",
               "Status": "CREATE_COMPLETE",
               "ChangeSetName": "SampleChangeSet-replacement",
               "CreationTime": "2020-11-18T21:03:37.706Z",
               "StackName": "SampleStack",
               "ChangeSetId": "arn:aws:cloudformation:us-east-1:123456789012:changeSet/SampleChangeSet-replacement/1a2345b6-0000-00a0-a123-00abc0abc000"
           }
       ]
   }
   ```

1. Run the [aws cloudformation describe\-change\-set](https://docs.aws.amazon.com/cli/latest/reference/cloudformation/describe-change-set.html) command, specifying the ID of the change set that you want to view\. For example:

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
       "CreationTime": "2020-11-18T23:35:25.813Z",
       "Capabilities": [],
       "StackName": "SampleStack",
       "NotificationARNs": [],
       "ChangeSetId": "arn:aws:cloudformation:us-east-1:123456789012:changeSet/SampleChangeSet-direct/9edde307-960d-4e6e-ad66-b09ea2f20255"
   }
   ```

   The `Changes` key lists changes to resources\. If you were to execute this change set, AWS CloudFormation would update the tags of the `i-1abc23d4` EC2 instance\. For a description of each field, see the [Change](https://docs.aws.amazon.com/AWSCloudFormation/latest/APIReference/API_Change.html) data type in the *AWS CloudFormation API Reference*\.

   For additional examples of change sets, see [Example change sets](using-cfn-updating-stacks-changesets-samples.md)\.