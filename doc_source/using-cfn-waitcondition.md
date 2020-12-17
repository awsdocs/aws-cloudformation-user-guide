# Creating wait conditions in a template<a name="using-cfn-waitcondition"></a>

**Important**  
For Amazon EC2 and Auto Scaling resources, we recommend that you use a CreationPolicy attribute instead of wait conditions\. Add a CreationPolicy attribute to those resources, and use the cfn\-signal helper script to signal when an instance creation process has completed successfully\.  
For more information, see [CreationPolicy](aws-attribute-creationpolicy.md) or [Deploying applications on Amazon EC2 with AWS CloudFormation](deploying.applications.md)\.

Using the [AWS::CloudFormation::WaitConditionHandle](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-waitconditionhandle.html) resource and [CreationPolicy](aws-attribute-creationpolicy.md) attribute, you can do the following:
+ Coordinate stack resource creation with other configuration actions that are external to the stack creation
+ Track the status of a configuration process

For example, you can start the creation of another resource after an application configuration is partially complete, or you can send signals during an installation and configuration process to track its progress\.

## Using a wait condition handle<a name="using-cfn-waitconditionhandle"></a>

**Note**  
If you use the [VPC endpoint](https://docs.aws.amazon.com/vpc/latest/userguide/vpc-endpoints.html) feature, resources in the VPC that respond to wait conditions must have access to AWS CloudFormation\-specific Amazon Simple Storage Service \(Amazon S3\) buckets\. Resources must send wait condition responses to a pre\-signed Amazon S3 URL\. If they can't send responses to Amazon S3, AWS CloudFormation won't receive a response and the stack operation fails\. For more information, see [Setting up VPC endpoints for AWS CloudFormation](cfn-vpce-bucketnames.md) and [Example bucket policies for VPC endpoints for Amazon S3](https://docs.aws.amazon.com/AmazonS3/latest/dev/example-bucket-policies-vpc-endpoint.html)\.

You can use the wait condition and wait condition handle to make AWS CloudFormation pause the creation of a stack and wait for a signal before it continues to create the stack\. For example, you might want to download and configure applications on an Amazon EC2 instance before considering the creation of that Amazon EC2 instance complete\.

The following list provides a summary of how a wait condition with a wait condition handle works:
+ AWS CloudFormation creates a wait condition just like any other resource\. When AWS CloudFormation creates a wait condition, it reports the wait condition’s status as CREATE\_IN\_PROGRESS and waits until it receives the requisite number of success signals or the wait condition’s timeout period has expired\. If AWS CloudFormation receives the requisite number of success signals before the time out period expires, it continues creating the stack; otherwise, it sets the wait condition’s status to CREATE\_FAILED and rolls the stack back\.
+ The `Timeout` property determines how long AWS CloudFormation waits for the requisite number of success signals\. `Timeout` is a minimum\-bound property, meaning the timeout occurs no sooner than the time you specify, but can occur shortly thereafter\. The maximum time that you can specify is 43200 seconds \(12 hours \)\.
+ Typically, you want a wait condition to begin immediately after the creation of a specific resource, such as an Amazon EC2 instance, RDS DB instance, or Auto Scaling group\. You do this by adding the [DependsOn attribute](aws-attribute-dependson.md) to a wait condition\. When you add a DependsOn attribute to a wait condition, you specify that the wait condition is created only after the creation of a particular resource has completed\. When the wait condition is created, AWS CloudFormation begins the timeout period and waits for success signals\.
+ You can also use the DependsOn attribute on other resources\. For example, you may want an RDS DB instance to be created and a database configured on that DB instance first before creating the EC2 instances that use that database\. In this case, you create a wait condition that has a DependsOn attribute that specifies the DB instance, and you create EC2 instance resources that have DependsOn attributes that specify the wait condition\. This would ensure that the EC2 instances would only be created directly after the DB instance and the wait condition were completed\.
+ AWS CloudFormation must receive a specified number of success signals for a wait condition before setting that wait condition’s status to CREATE\_COMPLETE continuing the creation of the stack\. The wait condition’s Count property specifies the number of success signals\. If none is set, the default is 1\.
+ A wait condition requires a wait condition handle to set up a presigned URL that is used as the signaling mechanism\. The presigned URL enables you to send a signal without having to supply your AWS credentials\. You use that presigned URL to signal success or failure, which is encapsulated in a JSON statement\. For the format of that JSON statement, see the [Wait condition signal JSON format](#using-cfn-waitcondition-signaljson)\.
+ If a wait condition receives the requisite number of success signals \(as defined in the Count property\) before the timeout period expires, AWS CloudFormation marks the wait condition as CREATE\_COMPLETE and continues creating the stack\. Otherwise, AWS CloudFormation fails the wait condition and rolls the stack back \(for example, if the timeout period expires without requisite success signals or if a failure signal is received\)\.

**To use a wait condition in a stack:**

1. Declare an AWS::CloudFormation::WaitConditionHandle resource in the stack's template\. A wait condition handle has no properties; however, a reference to a WaitConditionHandle resource resolves to a pre\-signed URL that you can use to signal success or failure to the WaitCondition\. For example:

   ```
   1. "myWaitHandle" : {
   2.      "Type" : "AWS::CloudFormation::WaitConditionHandle",
   3.      "Properties" : {
   4.      }
   5. }
   ```

1. Declare an AWS::CloudFormation::WaitCondition resource in the stack's template\. A WaitCondition resource has two required properties: Handle is a reference to a WaitConditionHandle declared in the template and Timeout is the number seconds for AWS CloudFormation to wait\. You can optionally set the Count property, which determines the number of success signals that the wait condition must receive before AWS CloudFormation can resume creating the stack\.

   To control when the wait condition is triggered, you set a DependsOn attribute on the wait condition\. A DependsOn clause associates a resource with the wait condition\. After AWS CloudFormation creates the DependsOn resource, it blocks further stack resource creation until one of the following events occur: a\) the timeout period expires b\) The requisite number of success signals are received c\) A failure signal is received\.

   Here is an example of a wait condition that begins after the successful creation of the Ec2Instance resource, uses the myWaitHandle resource as the WaitConditionHandle, has a timeout of 4500 seconds, and has the default Count of 1 \(since no Count property is specified\):

   ```
   1. "myWaitCondition" : {
   2.     "Type" : "AWS::CloudFormation::WaitCondition",
   3.     "DependsOn" : "Ec2Instance",
   4.     "Properties" : {
   5.         "Handle" : { "Ref" : "myWaitHandle" },
   6.         "Timeout" : "4500"
   7.     }
   8. }
   ```

1. Get the presigned URL to use for signaling\.

   In the template, the presigned URL can be retrieved by passing the logical name of the AWS::CloudFormation::WaitConditionHandle resource to the Ref intrinsic function\. For example, you can use the UserData property on AWS::EC2::Instance resources to pass the presigned URL to the Amazon EC2 instances so that scripts or applications running on those instances can signal success or failure to AWS CloudFormation:

   ```
   1. "UserData" : {
   2.    "Fn::Base64" : {
   3.        "Fn::Join" : [ "", ["SignalURL=", { "Ref" : "myWaitHandle" } ] ]
   4.    }
   5. }
   ```

   Note: In the AWS Management Console or the AWS CloudFormation command line tools, the presigned URL is displayed as the physical ID of the wait condition handle resource\.

1. Select a method for detecting when the stack enters the wait condition\.

   If you create the stack with notifications enabled, AWS CloudFormation publishes a notification for every stack event to the specified topic\. If you or your application subscribe to that topic, you can monitor the notifications for the wait condition handle creation event and retrieve the presigned URL from the notification message\.

   You can also monitor the stack's events using the AWS Management Console, the AWS CloudFormation command line tools, or the AWS CloudFormation API\.

1. Use the presigned URL to signal success or failure\.

   To send a signal, you send an HTTP request message using the presigned URL\. The request method must be PUT and the Content\-Type header must be an empty string or omitted\. The request message must be a JSON structure of the form specified in [Wait condition signal JSON format](#using-cfn-waitcondition-signaljson)\.

   You need to send the number of success signals specified by the Count property in order for AWS CloudFormation to continue stack creation\. If you have a Count that is greater than 1, the UniqueId value for each signal must be unique across all signals sent to a particular wait condition\. The UniqueId is an arbitrary alphanumerical string\.

   A Curl command is one way to send a signal\. The following example shows a Curl command line that signals success to a wait condition\.

   ```
   1. curl -T /tmp/a "https://cloudformation-waitcondition-test.s3.amazonaws.com/arn%3Aaws%3Acloudformation%3Aus-east-2%3A034017226601%3Astack%2Fstack-gosar-20110427004224-test-stack-with-WaitCondition--VEYW%2Fe498ce60-70a1-11e0-81a7-5081d0136786%2FmyWaitConditionHandle?Expires=1303976584&AWSAccessKeyId=AKIAIOSFODNN7EXAMPLE&Signature=ik1twT6hpS4cgNAw7wyOoRejVoo%3D"
   ```

   where the file /tmp/a contains the following JSON structure:

   ```
   1. {
   2.    "Status" : "SUCCESS",
   3.    "Reason" : "Configuration Complete",
   4.    "UniqueId" : "ID1234",
   5.    "Data" : "Application has completed configuration."
   6. }
   ```

   This example shows a Curl command line that sends the same success signal except it sends the JSON structure as a parameter on the command line\.

   ```
   1. curl -X PUT -H 'Content-Type:' --data-binary '{"Status" : "SUCCESS","Reason" : "Configuration Complete","UniqueId" : "ID1234","Data" : "Application has completed configuration."}' "https://cloudformation-waitcondition-test.s3.amazonaws.com/arn%3Aaws%3Acloudformation%3Aus-east-2%3A034017226601%3Astack%2Fstack-gosar-20110427004224-test-stack-with-WaitCondition--VEYW%2Fe498ce60-70a1-11e0-81a7-5081d0136786%2FmyWaitConditionHandle?Expires=1303976584&AWSAccessKeyId=AKIAIOSFODNN7EXAMPLE&Signature=ik1twT6hpS4cgNAw7wyOoRejVoo%3D"
   ```

### Wait condition signal JSON format<a name="using-cfn-waitcondition-signaljson"></a>

When you signal a wait condition, you must use the following JSON format:

```
1. {
2.   "Status" : "StatusValue",
3.   "UniqueId" : "Some UniqueId",
4.   "Data" : "Some Data",
5.   "Reason" : "Some Reason"
6. }
```

Where:

*StatusValue* must be one of the following values:
+ *SUCCESS* indicates a success signal\.
+ *FAILURE* indicates a failure signal and triggers a failed wait condition and a stack rollback\.

*UniqueId* identifies the signal to AWS CloudFormation\. If the Count property of the wait condition is greater than 1, the UniqueId value must be unique across all signals sent for a particular wait condition; otherwise, AWS CloudFormation will consider the signal a retransmission of the previously sent signal with the same UniqueId, and it will ignore the signal\.

*Data* is any information that you want to send back with the signal\. The Data value can be accessed by calling the [Fn::GetAtt function](intrinsic-function-reference-getatt.md) within the template\. For example, if you create the following output value for the wait condition mywaitcondition, you can use the `aws cloudformation describe-stacks` command, [DescribeStacks action](http://docs.aws.amazon.com/AWSCloudFormation/latest/APIReference/API_DescribeStacks.html), or Outputs tab of the CloudFormation console to view the Data sent by valid signals sent to AWS CloudFormation: 

```
"WaitConditionData" : {
  "Value" : { "Fn::GetAtt" : [ "mywaitcondition", "Data" ]},
  "Description" : "The data passed back as part of signalling the WaitCondition"
},
```

The Fn::GetAtt function returns the UniqueId and Data as a name/value pair within a JSON structure\. The following is an example of the Data attribute returned by the WaitConditionData output value defined above:

```
{"Signal1":"Application has completed configuration."}
```

*Reason* is a string with no other restrictions on its content besides JSON compliance\.