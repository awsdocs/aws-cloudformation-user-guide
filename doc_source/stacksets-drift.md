# Detecting unmanaged configuration changes in stack sets<a name="stacksets-drift"></a>

Even as you manage your stacks and the resources they contain through CloudFormation, users can change those resources outside of CloudFormation\. Users can edit resources directly by using the underlying service that created the resource\. By performing drift detection on a stack set, you can determine if any of the stack instances belonging to that stack set differ, or have *drifted*, from their expected configuration\.

## How CloudFormation performs drift detection on a stack set<a name="stacksets-drift-how"></a>

When CloudFormation performs drift detection on a stack set, it performs drift detection on the stack associated with each stack instance in the stack set\. To do this, CloudFormation compares the current state of each resource in the stack with the expected state of that resource, as defined in the stack's template and and any specified input parameters\. If the current state of a resource varies from its expected state, that resource is considered to have drifted\. If one or more resources in a stack have drifted, then the stack itself is considered to have drifted, and the stack instances that the stack is associated with is considered to have drifted as well\. If one or more stack instances in a stack set have drifted, the stack set itself is considered to have drifted\.

Drift detection identifies unmanaged changes; that is, changes made to stacks outside of CloudFormation\. Changes made through CloudFormation to a stack directly, rather than at the stack\-set level, are not considered drift\. For example, suppose you have a stack that is associated with a stack instance of a stack set\. If you use CloudFormation to update that stack to use a different template, that is not considered drift, even though that stack now has a different template than any other stacks belonging to the stack set\. This is because the stack still matches its expected template and parameter configuration in CloudFormation\. 

For detailed information on how CloudFormation performs drift detection on a stack, see [Detecting unmanaged configuration changes to stacks and resources](using-cfn-stack-drift.md)\.

Because CloudFormation performs drift detection on each stack individually, it takes any overridden parameter values into account when determining whether a stack has drifted\. For more information on overriding template parameters in stack instances, see [Override parameters on stack instances](stackinstances-override.md)\.

 If you perform drift detection [directly on a stack](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-stack-drift.html) that is associated with a stack instance, those drift results are not available from the **StackSets** console page\.

**To detect drift on a stack set using the AWS Management Console**

1. Open the AWS CloudFormation console at [https://console\.aws\.amazon\.com/cloudformation](https://console.aws.amazon.com/cloudformation/)\.

1. On the **StackSets** page, select the stack set on which you want to perform drift detection\.

1. From the **Actions** menu, select **Detect drifts**\.

   CloudFormation displays an information bar stating that drift detection has been initiated for the selected stack set\.

1. Optional: To monitor the progress of the drift detection operation: 

   1. Click the stack set name to display the **Stackset details** page\.

   1. Select the **Operations** tab, select the drift detection operation, and then select **View drift details**\.

   CloudFormation displays the **Operation details** dialog box\.

1. Wait until CloudFormation completes the drift detection operation\. When the drift detection operation completes, CloudFormation updates **Drift status** and **Last drift check time** for your stack set\. These fields are listed on the **Overview** tab of the **StackSet details** page for the selected stack set\.

   The drift detection operation may take some time, depending on the number of stack instances included in the stack set, as well as the number of resources included in the stack set\. You can only run a single drift detection operation on a given stack set at one time\. CloudFormation continues the drift detection operation even after you dismiss the information bar\.

1. To review the drift detection results for the stack instances in a stack set, select the **Stack instances** tab\. 

   The **Stack name** column lists the name of the stack associated with each stack instance, and the **Drift status** column lists the drift status of that stack\. A stack is considered to have drifted if one or more of its resources have drifted\.

1. To review the drift detection results for the stack associated with a specific stack instances:

   1. Note the **AWS account**, **Stack name**, and **AWS region** for the stack instance\.

   1. Open the AWS CloudFormation console at [https://console\.aws\.amazon\.com/cloudformation](https://console.aws.amazon.com/cloudformation/)\.

      Log into the AWS account containing the stack instance\.

   1. Select the AWS region containing the stack instance\.

   1. From the left\-hand navigation pane, select **Stacks**\.

   1. Select the stack you wish to view, and then select **Drifts**\.

      CloudFormation displays the **Drifts** page for the stack associated with the specified stack instance\.

   In the **Resource drift status** section, CloudFormation lists each stack resource, its drift status, and the last time drift detection was initiated on the resource\. The logical ID and physical ID of each resource is displayed to help you identify them\. In addition, for resources with a status of **MODIFIED**, CloudFormation displays resource drift details\. 

   You can sort the resources based on their drift status using the **Drift status** column\.

   1. To view the details on a modified resource\.

     1. With the modified resource selected, select **View drift details**\.

       CloudFormation displays the drift detail page for that resource\. This page lists the resource's expected and current property values, and any differences between the two\. 

       To highlight a difference, in the **Differences** section select the property name\.
       + Added properties are highlighted in green in the **Current** column of the **Details** section\.
       + Deleted properties are highlighted in red in the **Expected** column of the **Details** section\.
       + Properties whose value have been changed are highlighted in blue in the both **Expected** and **Current** columns\.  
![\[The Resource drift status section of the Drift Details page, which contains drift information for each resource in the stack that supports drift detection. Details include drift status and expected and current property values.\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/console-stacks-drifts-drift-details-differences-1.png)

**To detect drift on a stack set using the AWS CLI**

To detect drift on an entire stack using the AWS CLI, use the following `aws cloudformation` commands:
+ `[detect\-stack\-set\-drift](https://docs.aws.amazon.com/cli/latest/reference/cloudformation/detect-stack-set-drift.html)` to initiate a drift detection operation on a stack\.
+ `[describe\-stack\-set\-operation](https://docs.aws.amazon.com/cli/latest/reference/cloudformation/describe-stack-set-operation.html)` to monitor the status of the stack drift detection operation\.
+ Once the drift detection operation has completed, use the following commands to return drift information you want:
  + Use `[describe\-stack\-set](https://docs.aws.amazon.com/cli/latest/reference/cloudformation/describe-stack-set.html)` to return detailed information about the stack set, including detailed information about the last *completed* drift operation performed on the stack set\. \(Information about drift operations that are in progress is not included\.\)
  + Use `[list\-stackinstances](https://docs.aws.amazon.com/cli/latest/reference/cloudformation/list-stack-instances.html)` to return a list of stack instances belonging to the stack set, including the drift status and last drift time checked of each instance\.
  + Use `[describe\-stack\-instance](https://docs.aws.amazon.com/cli/latest/reference/cloudformation/describe-stack-instance.html)` to return detailed information about a specific stack instance, including its drift status and last drift time checked\.

1. Use `detect-stack-set-drift` to detect drift on an entire stack set and its associated stack instances\. 

   The following example initiates drift detection on the stack set `stack-set-drift-example`\.

   ```
   1. aws cloudformation detect-stack-set-drift --stack-set-name stack-set-drift-example
   2.             
   3. {
   4.     "OperationId": "c36e44aa-3a83-411a-b503-cb611example"
   5. }
   ```

1. Because stack set drift detection operations can be a long\-running operation, use `describe-stack-set-operation` to monitor the status of drift operation\. This command takes the stack set operation ID returned by the `detect-stack-set-drift` command\. 

   The following examples uses the operation ID from the previous example to return information on the stack set drift detection operation\. In this example, the operation is still running\. Of the seven stack instances associated with this stack set, one stack instance has already been found to have drifted, two instances are in synch, and drift detection for the remaining four stack instances is still in progress\. Since one instance has drifted, the drift status of the stack set itself is now `DRIFTED`\.

   ```
    1. aws cloudformation describe-stack-set-operation --stack-set-name stack-set-drift-example --operation-id c36e44aa-3a83-411a-b503-cb611example
    2.             
    3. {
    4.     "StackSetOperation": {
    5.         "Status": "RUNNING", 
    6.         "AdministrationRoleARN": "arn:aws:iam::012345678910:role/AWSCloudFormationStackSetAdministrationRole", 
    7.         "OperationPreferences": {
    8.             "RegionOrder": []
    9.         }, 
   10.         "ExecutionRoleName": "AWSCloudFormationStackSetExecutionRole", 
   11.         "StackSetDriftDetectionDetails": {
   12.             "DriftedStackInstancesCount": 1, 
   13.             "TotalStackInstancesCount": 7, 
   14.             "LastDriftCheckTimestamp": "2019-12-04T20:34:28.543Z", 
   15.             "InSyncStackInstancesCount": 2, 
   16.             "InProgressStackInstancesCount": 4, 
   17.             "DriftStatus": "DRIFTED", 
   18.             "FailedStackInstancesCount": 0
   19.         }, 
   20.         "Action": "DETECT_DRIFT", 
   21.         "CreationTimestamp": "2019-12-04T20:33:13.673Z", 
   22.         "StackSetId": "stack-set-drift-example:bd1f4017-d4f9-432e-a73f-8c22example", 
   23.         "OperationId": "c36e44aa-3a83-411a-b503-cb611example"
   24.     }
   25. }
   ```

   Performing the same command later, this example shows the information returned once the drift detection operation has completed\. Two of the seven total stack instances associated with this stack set have drifted, rendering the drift status of the stack set itself as `DRIFTED`\.

   ```
    1. aws cloudformation describe-stack-set-operation --stack-set-name stack-set-drift-example --operation-id c36e44aa-3a83-411a-b503-cb611example
    2.             
    3. {
    4.     "StackSetOperation": {
    5.         "Status": "SUCCEEDED", 
    6.         "AdministrationRoleARN": "arn:aws:iam::012345678910:role/AWSCloudFormationStackSetAdministrationRole", 
    7.         "OperationPreferences": {
    8.             "RegionOrder": []
    9.         }, 
   10.         "ExecutionRoleName": "AWSCloudFormationStackSetExecutionRole", 
   11.         "EndTimestamp": "2019-12-04T20:37:32.829Z", 
   12.         "StackSetDriftDetectionDetails": {
   13.             "DriftedStackInstancesCount": 2, 
   14.             "TotalStackInstancesCount": 7, 
   15.             "LastDriftCheckTimestamp": "2019-12-04T20:36:55.612Z", 
   16.             "InSyncStackInstancesCount": 5, 
   17.             "InProgressStackInstancesCount": 0, 
   18.             "DriftStatus": "DRIFTED", 
   19.             "FailedStackInstancesCount": 0
   20.         }, 
   21.         "Action": "DETECT_DRIFT", 
   22.         "CreationTimestamp": "2019-12-04T20:33:13.673Z", 
   23.         "StackSetId": "stack-set-drift-example:bd1f4017-d4f9-432e-a73f-8c22example", 
   24.         "OperationId": "c36e44aa-3a83-411a-b503-cb611example"
   25.     }
   26. }
   ```

1. When the stack set drift detection operation is complete, use the `describe-stack-set`, `list-stackinstances`, and `describe-stack-instance` commands to review the results\. 

   The `describe-stack-set` command includes the same detailed drift information returned by the `describe-stack-set-operation` command\.

   ```
   aws cloudformation describe-stack-set --stack-set-name stack-set-drift-example
               
               {
       "StackSet": {
           "Status": "ACTIVE", 
           "Description": "Demonstration of drift detection on stack sets.", 
           "Parameters": [], 
           "Tags": [
               {
                   "Value": "Drift detection", 
                   "Key": "Feature"
               }
           ], 
           "ExecutionRoleName": "AWSCloudFormationStackSetExecutionRole", 
           "Capabilities": [], 
           "AdministrationRoleARN": "arn:aws:iam::012345678910:role/AWSCloudFormationStackSetAdministrationRole", 
           "StackSetDriftDetectionDetails": {
               "DriftedStackInstancesCount": 2, 
               "TotalStackInstancesCount": 7, 
               "LastDriftCheckTimestamp": "2019-12-04T20:36:55.612Z", 
               "InProgressStackInstancesCount": 0, 
               "DriftStatus": "DRIFTED", 
               "DriftDetectionStatus": "COMPLETED", 
               "InSyncStackInstancesCount": 5, 
               "FailedStackInstancesCount": 0
           }, 
           "StackSetARN": "arn:aws:cloudformation:us-east-1:012345678910:stackset/stack-set-drift-example:bd1f4017-d4f9-432e-a73f-8c22example", 
           "TemplateBody": [details omitted], 
           "StackSetId": "stack-set-drift-example:bd1f4017-d4f9-432e-a73f-8c22ebexample", 
           "StackSetName": "stack-set-drift-example"
       }
   }
   ```

   You can use the `list-stack-instances` command to return summary information about the stack instances associated with a stack set, including the drift status of each stack instance\.

   In this example, executing `list-stack-instances` on the example stack set enables us to identify which two stack instances have a drift status of `DRIFTED`\.

   ```
   aws cloudformation list-stack-instances --stack-set-name stack-set-drift-example
                   
   {
       "Summaries": [
           {
               "StackId": "arn:aws:cloudformation:ap-northeast-1:012345678910:stack/StackSet-stack-set-drift-example-29168cdd-e587-4709-8a1f-90f752ec65e1/1a8a98f0-16d4-11ea-9844-060a5example", 
               "Status": "CURRENT", 
               "Account": "012345678910", 
               "Region": "ap-northeast-1", 
               "LastDriftCheckTimestamp": "2019-12-04T20:36:18.481Z", 
               "DriftStatus": "IN_SYNC", 
               "StackSetId": "stack-set-drift-example:bd1f4017-d4f9-432e-a73f-8c22eexample"
           }, 
           {
               "StackId": "arn:aws:cloudformation:eu-west-1:012345678910:stack/StackSet-stack-set-drift-example-b0fb6083-60c0-4e39-af15-2f071e0db90c/0e4f0940-16d4-11ea-93d8-0641cexample", 
               "Status": "CURRENT", 
               "Account": "012345678910", 
               "Region": "eu-west-1", 
               "LastDriftCheckTimestamp": "2019-12-04T20:37:32.687Z", 
               "DriftStatus": "DRIFTED", 
               "StackSetId": "stack-set-drift-example:bd1f4017-d4f9-432e-a73f-8c22eexample"
           }, 
           {
               "StackId": "arn:aws:cloudformation:us-east-1:012345678910:stack/StackSet-stack-set-drift-example-b7fde68e-e541-44c2-b33d-ef2e2988071a/008e6030-16d4-11ea-8090-12f89example", 
               "Status": "CURRENT", 
               "Account": "012345678910", 
               "Region": "us-east-1", 
               "LastDriftCheckTimestamp": "2019-12-04T20:34:28.275Z", 
               "DriftStatus": "DRIFTED", 
               "StackSetId": "stack-set-drift-example:bd1f4017-d4f9-432e-a73f-8c22eexample"
           }, 
           
           [additional stack instances omitted]
    
       ]
   }
   ```

   The `describe-stack-instance` command also returns this information, but for a single stack instance, as in the example below\.

   ```
   aws cloudformation describe-stack-instance --stack-set-name stack-set-drift-example --stack-instance-account 012345678910 --stack-instance-region us-east-1
               
   {
       "StackInstance": {
           "StackId": "arn:aws:cloudformation:us-east-1:012345678910:stack/StackSet-stack-set-drift-example-b7fde68e-e541-44c2-b33d-ef2e2988071a/008e6030-16d4-11ea-8090-12f89example", 
           "Status": "CURRENT", 
           "Account": "012345678910", 
           "Region": "us-east-1", 
           "ParameterOverrides": [], 
           "DriftStatus": "DRIFTED", 
           "LastDriftCheckTimestamp": "2019-12-04T20:34:28.275Z", 
           "StackSetId": "stack-set-drift-example:bd1f4017-d4f9-432e-a73f-8c22eexample"
       }
   }
   ```

1. Once you've identified which stack instances have drifted, you can use the information about the stack instances that is returned by the `list-stack-instances` or `describe-stack-instance` commands to execute the [describe\-stack\-resource\-drifts](https://docs.aws.amazon.com/cli/latest/reference/cloudformation/describe-stack-resource-drifts.html)\. This command returns detailed information about which resources in the stack have drifted\.

   The following example uses the stack ID of one of the drifted stacks, returned by the `list-stack-instances` command in the example above, to return detailed information about the resources that have been modified or deleted outside of CloudFormation\. In this stack, two properties on an `AWS::SQS::Queue` resource, `DelaySeconds` and `maxReceiveCount`, have been modified\.

   ```
   aws cloudformation describe-stack-resource-drifts --stack-name arn:aws:cloudformation:us-east-1:012345678910:stack/StackSet-stack-set-drift-example-b7fde68e-e541-44c2-b33d-ef2e2988071a/008e6030-16d4-11ea-8090-12f89example --stack-resource-drift-status-filters "MODIFIED" "DELETED"
                   
   {
       "StackResourceDrifts": [
           {
               "StackId": "arn:aws:cloudformation:us-east-1:012345678910:stack/StackSet-stack-set-drift-example-b7fde68e-e541-44c2-b33d-ef2e2988071a/008e6030-16d4-11ea-8090-12f8925a37c4", 
               "ActualProperties": "{\"DelaySeconds\":10,\"RedrivePolicy\":{\"deadLetterTargetArn\":\"arn:aws:sqs:us-east-1:012345678910:StackSet-stack-set-drift-example-b7fde68e-e541-44c2-b33d-ef2e2-DLQ-1H0SQCOKALBDJ\",\"maxReceiveCount\":20},\"VisibilityTimeout\":60}", 
               "ResourceType": "AWS::SQS::Queue", 
               "Timestamp": "2019-12-04T20:33:57.261Z", 
               "PhysicalResourceId": "https://sqs.us-east-1.amazonaws.com/012345678910/StackSet-stack-set-drift-example-b7fde68e-e541-44c2-b33d-ef2-Queue-6FNDEY4AUEPV", 
               "StackResourceDriftStatus": "MODIFIED", 
               "ExpectedProperties": "{\"DelaySeconds\":20,\"RedrivePolicy\":{\"deadLetterTargetArn\":\"arn:aws:sqs:us-east-1:012345678910:StackSet-stack-set-drift-example-b7fde68e-e541-44c2-b33d-ef2e2-DLQ-1H0SQCOKALBDJ\",\"maxReceiveCount\":10},\"VisibilityTimeout\":60}", 
               "PropertyDifferences": [
                   {
                       "PropertyPath": "/DelaySeconds", 
                       "ActualValue": "10", 
                       "ExpectedValue": "20", 
                       "DifferenceType": "NOT_EQUAL"
                   }, 
                   {
                       "PropertyPath": "/RedrivePolicy/maxReceiveCount", 
                       "ActualValue": "20", 
                       "ExpectedValue": "10", 
                       "DifferenceType": "NOT_EQUAL"
                   }
               ], 
               "LogicalResourceId": "Queue"
           }
       ]
   }
   ```

## Stopping drift detection on a stack set<a name="stacksets-drift-stop"></a>

Because drift detection on a stack set can be a long\-running operation, there may be instances when you want to stop a drift detection operation that is currently running on a stack set\.

**To stop drift detection on a stack set using the AWS Management Console**

1. Open the AWS CloudFormation console at [https://console\.aws\.amazon\.com/cloudformation](https://console.aws.amazon.com/cloudformation/)\.

1. On the **StackSets** page, select the name of the stack set\.

   CloudFormation displays the **StackSets details** page for the selected stack set\.

1. On the **StackSets details** page, select the **Operations** tab, and then select the drift detection operation\.

1. Select **Stop operation**\.

**To stop drift detection on a stack set using the the AWS CLI**
+ Use the `[stop\-stack\-set\-operation](https://docs.aws.amazon.com/cli/latest/reference/cloudformation/stop-stack-set-operation.html)` command\. You must supply both the stack set name and the operation ID of the drift detection stack set operation\.

  ```
  1. aws cloudformation stop-stack-set-operation --stack-set-name stack-set-drift-example --operation-id 624af370-311a-11e8-b6b7-500cexample
  ```