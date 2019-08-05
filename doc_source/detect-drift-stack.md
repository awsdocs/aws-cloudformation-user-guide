# Detect Drift on an Entire CloudFormation Stack<a name="detect-drift-stack"></a>

Performing a drift detection operation on a stack determines whether the stack has drifted from its expected template configuration, and returns detailed information about the drift status of each resource in the stack that supports drift detection\.

**To detect drift on an entire stack using the AWS Management Console**

1. Open the AWS CloudFormation console at [https://console\.aws\.amazon\.com/cloudformation](https://console.aws.amazon.com/cloudformation/)\.

1. From the list of stacks, select the stack on which you want to perform drift detection, choose **Actions**, and then choose **Detect drift for current stack**\.
![\[The Detect drift for current stack command selected on the Actions menu for the selected stack.\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/console-stacks-actions-detect-drift.png)

1. In the **Detect drift** dialog box, choose **Yes, detect**\.

   The **Detect drift** dialog box displays the **Detection status** as **DETECTION\_IN\_PROGRESS**\. The drift detection operation may take several minutes, depending on the number of resources included in the stack\. You can only run a single drift detection operation on a given stack at the same time\.

1. You can either leave the **Detect drift** dialog box open and view the details when CloudFormation completes drift detection, or you can close the dialog box and view the stack drift details later\. CloudFormation continues the drift detection operation even if you close the dialog box\.

   1. To view the drift detection details from the **Detect drift** dialog box:

      1. Wait until CloudFormation completes the drift detection operation\. When finished, AWS CloudFormation displays the **Detection status** as **DETECTION\_COMPLETE** and the appropriate **Drift status**\.

      1. Choose **View details** next to **Drift status**\.

   1. To close the **Detect drift** dialog box and view drift detection details later, choose **Close**\.

      Wait until CloudFormation completes the drift detection operation\. CloudFormation displays the appropriate **Drift status** when the operation completes\.

      1. To view drift detection details from the **Stacks** page:

         1. Click the stack for which you want to view drift detection details\.

         1. On the **Overview** tab, next to **Drift status**, click **View details**\.

            CloudFormation displays the **Drift Detail** page\.

      1. To view drift detection details from the **Stacks Detail** page:

         1. In the overview section, next to **Drift status**, click **View details**\.

           CloudFormation displays the **Drift Detail** page\.

1. Review the drift detection results for the stack and its resources\.

   In **Overview**, CloudFormation lists the overall drift status of the stack, as well as the last time drift detection was initiated on the stack or any of its individual resources\. A stack is considered to have drifted if one or more of its resources have drifted\.
![\[The Overview section of the Drift Details page for the selected stack, showing overall stack drift status, drift detection status, and the last time drift detection was initiated on the stack or any of its individual resources.\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/console-stacks-drifts-overview.png)

   In the **Resource drift details** section, CloudFormation lists each stack resource, its drift status, and the last time drift detection was initiated on the resource\. The logical ID and physical ID of each resource is displayed to help you identify them\. In addition, for resources with a status of **MODIFIED**, CloudFormation displays resource drift details\.

   1. To display resources based on their drift status\.

      1. For **Filter**, select the drift status for the resources you want to view\. To view all resources, select **All**\.
![\[The Resource drift status section of the Drift Details page, which contains drift information for each resource in the stack that supports drift detection. Details include drift status and expected and current property values.\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/console-stacks-drifts-resource-drift-status-filter.png)

   1. To view the details on a modified resource\.

      1. Choose the expand icon next to the resource's logical ID\.

        CloudFormation displays the resource's expected and current property values, and any differences between the two\.

        To highlight a difference, in the **Differences** column choose the property name, or **Select all**\.
        + Added properties are highlighted in green in the **Current** column\.
        + Deleted properties are highlighted in red in the **Expected** column\.
        + Properties whose value have been changed are highlighted in yellow in the both **Expected** and **Current** columns\.
![\[The Resource drift status section of the Drift Details page, which contains drift information for each resource in the stack that supports drift detection. Details include drift status and expected and current property values.\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/console-stacks-drifts-drift-details-differences.png)

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
