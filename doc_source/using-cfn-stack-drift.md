# Detecting Unmanaged Configuration Changes to Stacks and Resources<a name="using-cfn-stack-drift"></a>

Even as you manage your resources through CloudFormation, users can change those resources *outside* of CloudFormation\. Users can edit resources directly by using the underlying service that created the resource\. For example, you can use the Amazon EC2 console to update a server instance that was created as part of an CloudFormation stack\. Some changes may be accidental, and some may be made intentionally to respond to time\-sensitive operational events\. Regardless, changes made outside of CloudFormation can complicate stack update or deletion operations\. You can use drift detection to identify stack resources to which configuration changes have been made outside of CloudFormation management\. You can then take corrective action so that your stack resources are again in synch with their definitions in the stack template, such as updating the drifted resources directly so that they agree with their template definition\. Resolving drift helps to ensure configuration consistency and successful stack operations\.

**Topics**
+ [What Is Drift?](#what-is-drift)
+ [Drift Detection Status Codes](#drift-status-codes)
+ [Considerations When Detecting Drift](#drift-considerations)
+ [Detect Drift on an Entire CloudFormation Stack](detect-drift-stack.md)
+ [Detect Drift on Individual Stack Resources](detect-drift-resource.md)
+ [Resources that Support Drift Detection](using-cfn-stack-drift-resource-list.md)

## What Is Drift?<a name="what-is-drift"></a>

Drift detection enables you to detect whether a stack's actual configuration differs, or has *drifted*, from its expected configuration\. Use AWS CloudFormation to detect drift on an entire stack, or on individual resources within the stack\. A resource is considered to have drifted if any of its actual property values differ from the expected property values\. This includes if the property or resource has been deleted\. A stack is considered to have drifted if one or more of its resources have drifted\. 

In order to determine whether a resource has drifted, CloudFormation determines the expected resource property values, as defined in the stack template and any values specified as template parameters\. CloudFormation then compares those expected values with the actual values of those resource properties as they currently exist in the stack\. A resource is considered to have drifted if one or more of its properties have been deleted, or had their value changed\. 

AWS CloudFormation generates detailed information on each resource in the stack that has drifted\.

CloudFormation detects drift on those resources that support drift detection\. Resources that do not support drift detection are assigned a drift status of NOT\_CHECKED\. For a list of resources that support drift detection, see [Resources that Support Drift Detection](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-stack-drift-resource-list.html)\.

You can perform drift detection on stacks with the following statuses: `CREATE_COMPLETE`, `UPDATE_COMPLETE`, `UPDATE_ROLLBACK_COMPLETE`, and `UPDATE_ROLLBACK_FAILED`\.

When detecting drift on a stack, CloudFormation does not detect drift on any [nested stacks](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-nested-stacks.html) that belong to that stack\. Instead, you can initiate a drift detection operation directly on the nested stack\.

**Note**  
CloudFormation only determines drift for property values that are explicitly set, either through the stack template or by specifying template parameters\. This does not include default values for resource properties\. To have CloudFormation track a resource property for purposes of determining drift, explicitly set the property value, even if you are setting it to the default value\. 

## Drift Detection Status Codes<a name="drift-status-codes"></a>

The tables in this section describe the various status types used with drift detection:
+ **Drift detection operation status** describes the current state of the drift operation\.
+ **Stack drift status** describes the drift status of the stack as a whole, based on the drift status of its resources\.
+ **Resource drift status** describes the drift status of an individual resource\.

The following table lists the status codes CloudFormation assigns to stack drift detection operations\.


| Drift Detection Operation Status | Description | 
| --- | --- | 
|  `DETECTION_COMPLETE`  |  The stack drift detection operation has successfully completed for all resources in the stack that support drift detection\.   | 
|  `DETECTION_FAILED`  |  The stack drift detection operation has failed for at least one resource in the stack\. Results will be available for resources on which CloudFormation successfully completed drift detection\.  | 
|  `DETECTION_IN_PROGRESS`  |  The stack drift detection operation is currently in progress\.  | 

The following table lists the drift status codes CloudFormation assigns to stacks\.


| Stack Drift Status | Description | 
| --- | --- | 
|  `DRIFTED`  |  The stack differs, or has *drifted*, from its expected template configuration\. A stack is considered to have drifted if one or more of its resources have drifted\.  | 
|  `NOT_CHECKED`  |  AWS CloudFormation has not checked if the stack differs from its expected template configuration\.  | 
|  `IN_SYNC`  |  The current configuration of each supported resource matches its expected template configuration\. A stack with no resources that support drift detection will also have a status of IN\_SYNC\.  | 

The following table lists the drift status codes CloudFormation assigns to stack resources\.


| Resource Drift Status | Description | 
| --- | --- | 
|  `DELETED`  |  The resource differs from its expected template configuration because the resource has been deleted\.  | 
|  `MODIFIED`  |  The resource differs from its expected template configuration\.  | 
|  `NOT_CHECKED`  |  CloudFormation has not checked if the resource differs from its expected template configuration\.  | 
|  `IN_SYNC`  |  The resource’s current configuration matches its expected template configuration\.  | 

The following table lists the difference\-type status codes CloudFormation assigns to resource properties that differ from their expected template configuration\.


| Property Difference Types | Description | 
| --- | --- | 
|  `ADD`  |  A value has been added to a resource property that is an array or list data type\.   | 
|  `REMOVE`  |  The property has been removed from the current resource configuration\.  | 
|  `NOT_EQUAL`  |  The current property value differs from its expected value as defined in the stack template\.  | 

## Considerations When Detecting Drift<a name="drift-considerations"></a>

In order to successfully perform drift detection on a stack, a user must have the following permissions:
+ Read permission for each resource that supports drift detection included in the stack\. For example, if the stack includes an `AWS::EC2::Instance` resource, you must have `ec2:DescribeInstances` permission to perform drift detection on the stack\.
+ `cloudformation:DetectStackDrift`
+ `cloudformation:DetectStackResourceDrift`

For more information on setting permissions in CloudFormation, see [Controlling Access with AWS Identity and Access Management](using-iam-template.md)\.

In certain edge cases, CloudFormation may not be able to always return accurate drift results\. You should be aware of these edge cases in order to properly interpret your drift detection results\.
+ In certain cases, objects contained in property arrays will be reported as drift, when in actuality they are default values supplied to the property from the underlying service responsible for the resource\.
+ Certain resources have *attachment relationships* with related resources, such that a resource may actually attach or remove property values for another resource, defined in the same or another template\. For example, the `AWS::EC2::SecurityGroupIngress` and `AWS::EC2::SecurityGroupEgress` resources may be used to attach and remove values from `AWS::EC2::SecurityGroup` resources\. In these cases, CloudFormation analyses the stack template for attachments before performing the drift comparison\. However, CloudFormation cannot perform this analysis across stacks, and so may not return accurate drift results where resources that are attached reside in different stacks\.

  Resources that support drift detection and allow or require attachments from other resources include:    
[\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-stack-drift.html)
+ CloudFormation does not perform drift detection on the `KMSKeyId` property of any resources\. Because AWS KMS keys can be referenced by multiple aliases, CloudFormation cannot guarantee consistently accurate drift results for this property\. 
+ There are certain resource properties that you can specify in your stack template that, by their very nature, CloudFormation will not be able to compare to the properties in the resulting stack resources\. These properties therefore cannot be included in drift detection results\. Such properties fall into two broad categories:
  + Property values that CloudFormation cannot map back to their initial resource property value in the stack template\.

    For example, CloudFormation cannot map the source code of a Lambda function back to the [Code](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-lambda-function-code.html) property type of the [Function](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-lambda-function.html) resource, and therefore CloudFormation cannot include it in drift detection results\. 
  + Property values that the service that is responsible for the resource does not return\.

    There are certain property values that, by design, are never returned by the service to which the resource belongs\. These tend to contain confidential information, such as passwords or other sensitive data that should not be exposed\. For example, the IAM service will never return the value of the `Password` property of the [IAM User LoginProfile](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-iam-user-loginprofile.html) property type, and therefore CloudFormation cannot include it in drift detection results\. 
  + Objects in an array: they may be actually service defaults, not drift added manually out\-of\-band\.
+ Drift detection is available in the US East \(N\. Virginia\), US East \(Ohio\), US West \(N\. California\), US West \(Oregon\), Canada \(Central\), Asia Pacific \(Mumbai\), Asia Pacific \(Seoul\), Asia Pacific \(Singapore\), Asia Pacific \(Sydney\), Asia Pacific \(Tokyo\), Europe \(Frankfurt\), Europe \(Ireland\), Europe \(London\), Europe \(Paris\), and South America \(São Paulo\) regions\.
+ If you encounter any false positive, send us your comments using the feedback link in the CloudFormation console, or reach out to us via the AWS forums at [https://forums\.aws\.amazon\.com](https://forums.aws.amazon.com)\.