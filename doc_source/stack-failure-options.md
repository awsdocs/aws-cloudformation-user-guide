# Stack failure options<a name="stack-failure-options"></a>

You can iteratively develop your applications when provisioning failures are encountered by starting from the point of failure without rolling back successfully provisioned resources\. By specifying stack failure options, you can troubleshoot resources in a `CREATE_FAILED` or `UPDATE_FAILED` status\. You can provision failure options for all stack deployments and change set operations\.
+ Create operations set to **Preserve successfully provisioned resources** preserves the state of successful resources, while failed resources will stay in a failed state until the next update operation is performed\.
+ Update and change set operations set to **Preserve successfully provisioned resources** preserves the state of successful resources while rolling back failed resources to the last known stable state\. Failed resources will be in an `UPDATE_FAILED` state\. Resources without a last known stable state will be deleted upon the next stack operation\.

See the following sections for more details about pausing the rollback of failed resources:
+ [Overview of stack failure options](#stack-failure-options-overview)
+ [Conditions to pause stack rollback](#stack-failure-options-conditions)
+ [Preserve successfully provisioned resources \(console\)](#stack-failure-options-console)
+ [Preserve successfully provisioned resources \(AWS CLI\)](#stack-failure-options-cli)

## Overview of stack failure options<a name="stack-failure-options-overview"></a>

Before issuing an operation from the AWS CloudFormation console, API, or AWS Command Line Interface \(AWS CLI\), specify the behavior for provisioned resource failure\. Then, proceed with the deployment process of your resources without any other modifications\. In the event of an operational failure, CloudFormation stops at the first failure in each independent provisioning path\. CloudFormation identifies dependencies between resources to parallelize independent provisioning actions\. Then it proceeds to provision resources on each independent provisioning path until it encounters a failure\. A failure in one path doesn’t affect other provisioning paths\. CloudFormation will continue to provision the resources until completion or stop on a different failure\.

Remediate any issues to continue the deployment process\. CloudFormation performs the necessary updates before retrying provisioning actions on resources that couldn’t be successfully provisioned earlier\. You remediate issues by submitting a **Retry**, **Update**, or **Roll back** operations\. For example, if you're provisioning an Amazon EC2 instance and the EC2 instance fails during a create operation, you might want to investigate the error, rather than rolling back the failed resource right away\. You can review system status checks and instances status checks, and then select the **Retry** operation once the issues is resolved\.

When a stack operation fails, and you've specified **Preserve successfully provisioned resources** from the **Stack failure options** menu, you can select the following options\.
+ **Retry** – Retries provisioning operation on failed resources and continues provisioning the template until the successful completion of the stack operation or the next failure\. Select this option if the resource failed to provision due to an issue that doesn't require template modifications, such as an AWS Identity and Access Management \(IAM\) permission\.
+ **Update** – Resources that have been provisioned are updated on template updates\. Resources that failed to create or update will be retried\. Select this option if the resource failed to provision due to template errors, and you've modified the template\. When you update a stack that's in a `FAILED` state, you must select **Preserve successfully provisioned resources** for the **Stack failure options** to continue updating your stack\.
+ **Roll back** – CloudFormation rolls back the stack to the last known stable state\.

## Conditions to pause stack rollback<a name="stack-failure-options-conditions"></a>

To pause the rollback of failed resources in your stack, the following conditions must be met\.
+ You must specify the **Preserve successfully provisioned resources** parameter during a stack operation\. For more information about rollback behavior, see [Setting AWS CloudFormation stack options](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/cfn-console-add-tags.html#rollback)\.
+ A stack operation must have a stack status of `CREATE_FAILED` or `UPDATE_FAILED`\. For information about stack status, see [Stack status codes](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-describing-stacks.html#w2ab1c23c15c17c11)\.

**Note**  
Immutable update types aren't supported\.

## Preserve successfully provisioned resources \(console\)<a name="stack-failure-options-console"></a>

------
#### [ Create stack ]

**To preserve successfully provisioned resources during a create stack operation**

1. Sign in to the AWS Management Console and open the AWS CloudFormation console at [https://console\.aws\.amazon\.com/cloudformation](https://console.aws.amazon.com/cloudformation/)\.

1. Choose **Create stack** and select **With new resources \(standard\)**\.

1. On the **Specify template** page, choose a stack template by using one of the following options:
   + **Template is ready**
   + **Use a sample template**
   + **Create template in Designer**

   Accept your settings and select **Next**\.

1. On the **Specify stack details** page, enter a stack name in the **Stack name** box\.

1. In the **Parameters** section, specify parameters that are defined in your stack template\.

   You can use or change any parameters with default values\.

1. When you're satisfied with the parameter values, choose **Next**\.

1. On the **Configure stack options** page, you can set additional options for your stack\.

1. For **Stack failure options**, select **Preserve successfully provisioned resources**\.

1. When you're satisfied with the stack options, choose **Next**\.

1. Review your stack on the **Review** page and select **Create stack**\.

*Results*: Resources that failed to create transition the stack status to `CREATE_FAILED` to prevent the stack from rolling back when the stack operation encounters a failure\. Resources that are successfully provisioned are in a `CREATE_COMPLETE` state\. You can monitor the stack in the **Stack events** tab\.

------
#### [ Update stack ]

**To preserve successfully provisioned resources during an update stack operation**

1. Sign in to the AWS Management Console and open the AWS CloudFormation console at [https://console\.aws\.amazon\.com/cloudformation](https://console.aws.amazon.com/cloudformation/)\.

1. Select the stack you want to update and then choose **Update**\.

1. On the **Update stack** page, choose a stack template by using one of the following options:
   + **Use current template**
   + **Replace current template**
   + **Edit template in designer**

   Accept your settings and select **Next**\.

1. On the **Specify stack details** page, specify parameters that are defined in your stack template\.

   You can use or change any parameters with default values\.

1. When you're satisfied with the parameter values, choose **Next**\.

1. On the **Configure stack options** page, you can set additional options for your stack\.

1. For the **Behavior on provisioning failure**, select **Preserve successfully provisioned resources**\.

1. When you're satisfied with the stack options, choose **Next**\.

1. Review your stack on the **Review** page and select **Update stack**\.

*Results*: Resources that failed to update transition the stack status to `UPDATE_FAILED` and roll back to the last known stable state\. Resources without a last known stable state will be deleted by CloudFormation upon the next stack operation\. Resources that are successfully provisioned are in a `CREATE_COMPLETE` or `UPDATE_COMPLETE` state\. You can monitor the stack in the **Stack events** tab\.

------
#### [ Change set ]

**Note**  
You can initiate a change set for a stack with a status of `CREATE_FAILED` or `UPDATE_FAILED`, but not for a status of `UPDATE_ROLLBACK_FAILED`\.

**To Preserve successfully provisioned resources during a change set operation**

1. Sign in to the AWS Management Console and open the AWS CloudFormation console at [https://console\.aws\.amazon\.com/cloudformation](https://console.aws.amazon.com/cloudformation/)\.

1. Select the stack that contains the change set you want to initiate, and then choose the **Change sets** tab\.

1. Select the change set and then choose **Execute**\.

1. For **Execute change set**, select the **Preserve successfully provisioned resources** option\.

1. Select **Execute change set**\.

*Results*: Resources that failed to update transition the stack status to `UPDATE_FAILED` and roll back to the last known stable state\. Resources without a last known stable state will be deleted by CloudFormation upon the next stack operation\. Resources that are successfully provisioned are in a `CREATE_COMPLETE` or `UPDATE_COMPLETE` state\. You can monitor the stack in the **Stack events** tab\.

------

## Preserve successfully provisioned resources \(AWS CLI\)<a name="stack-failure-options-cli"></a>

------
#### [ Create stack ]

**To preserve successfully provisioned resources during a stack create operation**

Specify the `disable-rollback` option or `on-failure DO_NOTHING` enumeration during a [create\-stack](https://docs.aws.amazon.com/cli/latest/reference/cloudformation/create-stack.html) operation\.

1. Provide a stack name and template to the `create-stack` command with the `disable-rollback` option\.

   ```
   aws cloudformation create-stack --stack-name myteststack --template-body file://DOC-EXAMPLE-BUCKET.json --disable-rollback
   ```

   The command returns the following output\.

   ```
   {
       "StackId": "arn:aws:cloudformation:us-east-1:123456789012:stack/myteststack/466df9e0-0dff-08e3-8e2f-5088487c4896"
   }
   ```

1. Describe the state of the stack using the `describe-stacks` option\.

   ```
   aws cloudformation describe-stacks --stack-name myteststack
   ```

   The command returns the following output\.

   ```
   {
       "Stacks":  [
           {
               "StackId": "arn:aws:cloudformation:us-east-1:123456789012:stack/myteststack/466df9e0-0dff-08e3-8e2f-5088487c4896",
               "Description": "AWS CloudFormation Sample Template",
               "Tags": [],
               "Outputs": [],
               "StackStatusReason": “The following resource(s) failed to create: [MyBucket]”,
               "CreationTime": "2013-08-23T01:02:15.422Z",
               "Capabilities": [],
               "StackName": "myteststack",
               "StackStatus": "CREATE_FAILED",
               "DisableRollback": true
           }
       ]
   }
   ```

------
#### [ Update stack ]

**To preserve successfully provisioned resources during a stack update operation\.**

1. Provide an existing stack name and template to the `update-stack` command with the `disable-rollback` option\.

   ```
   aws cloudformation update-stack --stack-name myteststack --template-url DOC-EXAMPLE-BUCKET.template --disable-rollback
   ```

   The command returns the following output\.

   ```
   {
       "StackId": "arn:aws:cloudformation:us-east-1:123456789012:stack/myteststack/466df9e0-0dff-08e3-8e2f-5088487c4896"
   }
   ```

1. Describe the state of the stack using either the `describe-stacks` or `describe-stack-events` option\.

   ```
   aws cloudformation describe-stacks --stack-name myteststack
   ```

   The command returns the following output\.

   ```
   {
       "Stacks":  [
           {
               "StackId": "arn:aws:cloudformation:us-east-1:123456789012:stack/myteststack/466df9e0-0dff-08e3-8e2f-5088487c4896",
               "Description": "AWS CloudFormation Sample Template",
               "Tags": [],
               "Outputs": [],
               "CreationTime": "2013-08-23T01:02:15.422Z",
               "Capabilities": [],
               "StackName": "myteststack",
               "StackStatus": "UPDATE_COMPLETE",
               "DisableRollback": true
           }
       ]
   }
   ```

------
#### [ Change set ]

**Note**  
You can initiate a change set for a stack with a status of `CREATE_FAILED` or `UPDATE_FAILED` but not for a status of `UPDATE_ROLLBACK_FAILED`\.

**To preserve successfully provisioned resources during a change set operation**

Specify the `disable-rollback` option  during an [execute\-change\-set](https://docs.aws.amazon.com/cli/latest/reference/cloudformation/execute-change-set.html) operation\.

1. Provide a stack name and template to the `execute-change-set` command with the `disable-rollback` option\.

   ```
   aws cloudformation execute-change-set --stack-name myteststack --change-set-name my-change-set --template-body file://template.yaml
   ```

   The command returns the following output\.

   ```
   {
    "Id": "arn:aws:cloudformation:us-east-1:123456789012:changeSet/my-change-set/bc9555ba-a949-xmpl-bfb8-f41d04ec5784",
    "StackId": "arn:aws:cloudformation:us-east-1:123456789012:stack/myteststack/466df9e0-0dff-08e3-8e2f-5088487c4896"
   }
   ```

1. Initiate the change set with `disable-rollback` option\.

   ```
   aws cloudformation execute-change-set --stack-name myteststack --change-set-name my-change-set -–disable-rollback
   ```

1. Determine the status of the stack using either the `describe-stacks` or `describe-stack-events` option\.

   ```
   {
      "StackEvents": [
        {
           "StackId": "arn:aws:cloudformation:us-east-1:123456789012:stack/myteststack/466df9e0-0dff-08e3-8e2f-5088487c4896",
           "EventId": "49c966a0-7b74-11ea-8071-024244bb0672",
           "StackName": "myteststack",
           "LogicalResourceId": " MyBucket",
           "PhysicalResourceId": "MyBucket",
           "ResourceType": "AWS::S3::Bucket",
           "Timestamp": "2020-04-10T21:43:17.015Z",
           "ResourceStatus": "UPDATE_FAILED"
           "ResourceStatusReason": "User XYZ is not allowed to perform S3::UpdateBucket on MyBucket"
        }
   }
   ```

1. Fix permissions errors and retry the operation\.

   ```
   aws cloudformation update-stack --stack-name myteststack --use-previous-template --disable-rollback
   ```

   The command returns the following output\.

   ```
   {
       "StackId": "arn:aws:cloudformation:us-east-1:123456789012:stack/myteststack/466df9e0-0dff-08e3-8e2f-5088487c4896"
   }
   ```

1. Describe the state of the stack using either the `describe-stacks` or `describe-stack-events` option\.

   ```
   aws cloudformation describe-stacks --stack-name myteststack
   ```

   The command returns the following output\.

   ```
   {
       "Stacks":  [
           {
               "StackId": "arn:aws:cloudformation:us-east-1:123456789012:stack/myteststack/466df9e0-0dff-08e3-8e2f-5088487c4896",
               "Description": "AWS CloudFormation Sample Template",
               "Tags": [],
               "Outputs": [],
               "CreationTime": "2013-08-23T01:02:15.422Z",
               "Capabilities": [],
               "StackName": "myteststack",
               "StackStatus": "UPDATE_COMPLETE",
               "DisableRollback": true
           }
       ]
   }
   ```

------

### Roll back stack<a name="roll-back-stack-cli"></a>

**To roll back a stack from the CREATE\_FAILED or UPDATE\_FAILED stack status**

Specify the `rollback-stack` operation to roll back a stack to its last stable state\.
+ Initiate a rollback with the `rollback-stack` operation and specify the stack name\.

  ```
  aws cloudformation rollback-stack --stack-name myteststack
  ```

  The command returns the following output\.

  ```
  {
      "StackId": "arn:aws:cloudformation:us-east-1:123456789012:stack/myteststack/466df9e0-0dff-08e3-8e2f-5088487c4896"
  }
  ```

**Note**  
The `rollback-stack` operation will delete a stack if it doesn't contain a last known stable state\.