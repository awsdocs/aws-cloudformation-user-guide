# Configuring a target account gate in AWS CloudFormation StackSets<a name="stacksets-account-gating"></a>

An account gate is an optional feature that lets you specify an [AWS Lambda](http://docs.aws.amazon.com/lambda/latest/dg/lambda-introduction-function.html) function to verify that a target account meets certain requirements before AWS CloudFormation StackSets begins stack operations in that account\. A common example of an account gate is verifying that there are no CloudWatch alarms active or unresolved on the target account\. StackSets invokes the function each time you start stack operations in the target account, and only continues if the function returns a `SUCCEEDED` code\. If the Lambda function returns a status of `FAILED`, StackSets does not continue with your requested operation\. If you do not have an account gating Lambda function configured, StackSets skips the check, and continues with your operation\.

If your target account fails an account gate check, the failed operation counts toward your specified failure tolerance number or percentage of stacks\. For more information about failure tolerance, see [Stack set operation options](stacksets-concepts.md#stackset-ops-options)\.

Account gating is only available for StackSets operations\. This functionality is not available for other AWS CloudFormation operations outside of StackSets\.

## Setup requirements<a name="stacksets-accountgating_reqs"></a>

The following list describes setup requirements for account gating\.
+ To work with the StackSets account gating functionality, your Lambda function must be named **AWSCloudFormationStackSetAccountGate**\.
+ The **AWSCloudFormationStackSetExecutionRole** needs permissions to invoke your Lambda function\. Without these permissions, StackSets skips the account gating check, and continues with stack operations\.
+ The Lambda `InvokeFunction` permission must be added to target accounts for account gating to work\. The target account trust policy must have a trust relationship with the administrator account\. The following is an example of a policy statement that grants Lambda `invokefunction` permissions\.

  ```
  {
      "Version": "2012-10-17",
      "Statement": [
          {
              "Effect": "Allow",
              "Action": [
                  "lambda:InvokeFunction"
              ],
              "Resource": "*"
          }
      ]
  }
  ```

## Sample Lambda account gating functions<a name="stacksets-sample-accountgate"></a>

The following sample AWS CloudFormation templates are available for you to create Lambda **AWSCloudFormationStackSetAccountGate** functions\. For more information about how to create a new stack using either of these templates, see [Creating a stack](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/cfn-console-create-stack.html) in this guide\.


|  Template location  |  Description  | 
| --- | --- | 
|  [https://s3\.amazonaws\.com/cloudformation\-stackset\-templates\-us\-east\-1/cloudformation\-stack\-set\-accountgate\-succeeded\.template](https://s3.amazonaws.com/cloudformation-stackset-templates-us-east-1/cloudformation-stack-set-accountgate-succeeded.template)  |  Creates a stack that implements a Lambda account gate function that will return a status of `SUCCEEDED`\.  | 
|  [https://s3\.amazonaws\.com/cloudformation\-stackset\-templates\-us\-east\-1/cloudformation\-stack\-set\-accountgate\-failed\.template](https://s3.amazonaws.com/cloudformation-stackset-templates-us-east-1/cloudformation-stack-set-accountgate-failed.template)  |  Creates a stack that implements a Lambda account gate function that will return a status of `FAILED`\.  | 