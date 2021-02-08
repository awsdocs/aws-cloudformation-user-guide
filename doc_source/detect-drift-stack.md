# Detect drift on an entire CloudFormation stack<a name="detect-drift-stack"></a>

Performing a drift detection operation on a stack determines whether the stack has drifted from its expected template configuration, and returns detailed information about the drift status of each resource in the stack that supports drift detection\. 

**To detect drift on an entire stack using the AWS Management Console**

1. Open the AWS CloudFormation console at [https://console\.aws\.amazon\.com/cloudformation](https://console.aws.amazon.com/cloudformation/)\.

1. From the list of stacks, select the stack on which you want to perform drift detection\. In the stack details pane, choose **Stack actions**, and then choose **Detect drift**\.   
![\[The Detect drift for current stack command selected on the Stack actions menu for the selected stack.\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/console-stacks-actions-detect-drift-1.png)

   CloudFormation displays an information bar stating that drift detection has been initiated for the selected stack\.

1. Wait until CloudFormation completes the drift detection operation\. When the drift detection operation completes, CloudFormation updates **Drift status** and **Last drift check time** for your stack\. These fields are listed in the **Overview** section of the **Stack info** pane of the stack details page\.

   The drift detection operation may take several minutes, depending on the number of resources included in the stack\. You can only run a single drift detection operation on a given stack at the same time\. CloudFormation continues the drift detection operation even after you dismiss the information bar\.

1. Review the drift detection results for the stack and its resources\. With your stack selected, from the **Stack actions** menu select **View drift results**\.

   CloudFormation lists the overall drift status of the stack, as well as the last time drift detection was initiated on the stack or any of its individual resources\. A stack is considered to have drifted if one or more of its resources have drifted\.   
![\[The Drifts page for the selected stack, showing overall stack drift status, drift detection status, and the last time drift detection was initiated on the stack or any of its individual resources.\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/console-stacks-drifts-overview-1.png)

   In the **Resource drift status** section, CloudFormation lists each stack resource, its drift status, and the last time drift detection was initiated on the resource\. The logical ID and physical ID of each resource is displayed to help you identify them\. In addition, for resources with a status of **MODIFIED**, CloudFormation displays resource drift details\. 

   You can sort the resources based on their drift status using the **Drift status** column\.

   1. To view the details on a modified resource\.

     1. With the modified resource selected, select View drift details\.

       CloudFormation displays the drift detail page for that resource\. This page lists the resource's expected and current property values, and any differences between the two\. 

       To highlight a difference, in the **Differences** section select the property name\.
       + Added properties are highlighted in green in the **Current** column of the **Details** section\.
       + Deleted properties are highlighted in red in the **Expected** column of the **Details** section\.
       + Properties whose value have been changed are highlighted in yellow in the both **Expected** and **Current** columns\.  
![\[The Resource drift status section of the Drift Details page, which contains drift information for each resource in the stack that supports drift detection. Details include drift status and expected and current property values.\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/console-stacks-drifts-drift-details-differences-1.png)

**To detect drift on an entire stack using the AWS CLI**

To detect drift on an entire stack using the AWS CLI, use the following `aws cloudformation` commands:
+ `detect-stack-drift` to initiate a drift detection operation on a stack\.
+ `describe-stack-drift-detection-status` to monitor the status of the stack drift detection operation\.
+ `describe-stack-resource-drifts` to review the details of the stack drift detection operation\.

1. Use the `detect-stack-drift` to detect drift on an entire stack\. Specify the stack name or ARN\. You can also specify the logical IDs of any specific resources that you want to use as filters for this drift detection operation\.

   ```
   1. PROMPT> aws cloudformation detect-stack-drift --stack-name my-stack-with-resource-drift
   2. {
   3.     "StackDriftDetectionId": "624af370-311a-11e8-b6b7-500cexample"
   4. }
   ```

1. Because stack drift detection operations can be long\-running, use `describe-stack-drift-detection-status` to monitor the status of drift operation\. This command takes the stack drift detection ID returned by the `detect-stack-drift` command\. 

   In the example below, we've taken the stack drift detection ID returned by the `detect-stack-drift` example above and passed it as a parameter to `describe-stack-drift-detection-status`\. The parameter returns operation details that show that the drift detection operation has completed, a single stack resource has drifted, and that the entire stack is considered to have drifted as a result\. 

   ```
   1. PROMPT> aws cloudformation describe-stack-drift-detection-status --stack-drift-detection-id 624af370-311a-11e8-b6b7-500cexample
   2. {
   3.     "StackId": "arn:aws:cloudformation:us-east-1:099908667365:stack/my-stack-with-resource-drift/489e5570-df85-11e7-a7d9-50example", 
   4.     "StackDriftDetectionId": "624af370-311a-11e8-b6b7-500cexample", 
   5.     "StackDriftStatus": "DRIFTED", 
   6.     "Timestamp": "2018-03-26T17:23:22.279Z", 
   7.     "DetectionStatus": "DETECTION_COMPLETE", 
   8.     "DriftedStackResourceCount": 1
   9. }
   ```

1. When the stack drift detection operation is complete, use the `describe-stack-resource-drifts` command to review the results, including actual and expected property values for resources that have drifted\. 

   The example below uses the `stack-resource-drift-status-filters` parameter to request stack drift information for those resources that have been modified or deleted\. The request returns information on the one resource that has been modified, including details about two of its properties whose values have been changed\. No resources have been deleted\.

   ```
    1. PROMPT> aws cloudformation describe-stack-resource-drifts --stack-name my-stack-with-resource-drift --stack-resource-drift-status-filters MODIFIED DELETED
    2. {
    3.     "StackResourceDrifts": [
    4.         {
    5.             "StackId": "arn:aws:cloudformation:us-east-1:099908667365:stack/my-stack-with-resource-drift/489e5570-df85-11e7-a7d9-50example", 
    6.             "ActualProperties": "{\"ReceiveMessageWaitTimeSeconds\":0,\"DelaySeconds\":120,\"RedrivePolicy\":{\"deadLetterTargetArn\":\"arn:aws:sqs:us-east-1:099908667365:my-stack-with-resource-drift-DLQ-1BCY7HHD5QIM3\",\"maxReceiveCount\":12},\"MessageRetentionPeriod\":345600,\"MaximumMessageSize\":262144,\"VisibilityTimeout\":60,\"QueueName\":\"my-stack-with-resource-drift-Queue-494PBHCO76H4\"}", 
    7.             "ResourceType": "AWS::SQS::Queue", 
    8.             "Timestamp": "2018-03-26T17:23:34.489Z", 
    9.             "PhysicalResourceId": "https://sqs.us-east-1.amazonaws.com/099908667365/my-stack-with-resource-drift-Queue-494PBHCO76H4", 
   10.             "StackResourceDriftStatus": "MODIFIED", 
   11.             "ExpectedProperties": "{\"ReceiveMessageWaitTimeSeconds\":0,\"DelaySeconds\":20,\"RedrivePolicy\":{\"deadLetterTargetArn\":\"arn:aws:sqs:us-east-1:099908667365:my-stack-with-resource-drift-DLQ-1BCY7HHD5QIM3\",\"maxReceiveCount\":10},\"MessageRetentionPeriod\":345600,\"MaximumMessageSize\":262144,\"VisibilityTimeout\":60,\"QueueName\":\"my-stack-with-resource-drift-Queue-494PBHCO76H4\"}", 
   12.             "PropertyDifferences": [
   13.                 {
   14.                     "PropertyPath": "/DelaySeconds", 
   15.                     "ActualValue": "120", 
   16.                     "ExpectedValue": "20", 
   17.                     "DifferenceType": "NOT_EQUAL"
   18.                 }, 
   19.                 {
   20.                     "PropertyPath": "/RedrivePolicy/maxReceiveCount", 
   21.                     "ActualValue": "12", 
   22.                     "ExpectedValue": "10", 
   23.                     "DifferenceType": "NOT_EQUAL"
   24.                 }
   25.             ], 
   26.             "LogicalResourceId": "Queue"
   27.         }
   28.     ]
   29. }
   ```