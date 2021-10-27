# Importing a stack into AWS CloudFormation StackSets<a name="stacksets-import"></a>

The AWS CloudFormation *stack import* operation can import existing stacks into new or existing stack sets, so that you can migrate existing stacks to a stack set in one operation\. *StackSets* extends the functionality of stacks, so you can create, update, or delete stacks across multiple accounts and Regions with a single operation\. Use the stack import operation to import up to 10 stacks into a new stack set in the same account as the source stack or in a different administrator account and Region, by specifying the stack ID of the stack you intend to import\. Stack import is available wherever StackSets are supported\. For information about StackSets Region support, see [StackSets regional support](https://docs.aws.amazon.com/general/latest/gr/cfn.html#regional-support-stacksets)\.

For example, if you have a stack that specifies an administrator AWS Identity and Access Management \(IAM\) role across multiple accounts, you can import that stack into a stack set\. By using stack import, you avoid downtime and outages without deleting and recreating those resources\. Once the stack is imported into a stack set, the original stack will become a stack instance of the newly generated stack set\.

**Topics**
+ [Requirements for stack import](#stackset-import-considerations)
+ [Importing a stack into a stack set \(console\)](#importing-stack-to-stackset)
+ [Importing a stack into a stack set \(AWS CLI\)](#importing-stack-to-stackset.cli)
+ [Reverting a stack import operation](#reverting-stackset-import)

## Requirements for stack import<a name="stackset-import-considerations"></a>

Before you import a stack into a stack set, make sure you understand the following requirements:
+ The stack import feature requires an administrator account in which you create a stack set and a target account that contains a stack\.
+ The target account must have permission to use the `GetTemplate` operation with the input of stack ID or ARN\. Because of that, your administrator account must be granted **AWSCloudFormationStackSetsAdminstration** or **AWSCloudFormationStackSetsExectionRole** permissions\.
+ Stacks can only belong to one stack set\.
+ You can implement stack tags to the stack set by specifying tags explicitly as parameters in the stack import operation\.
+ A stack's custom parameter overrides aren't affected during the import operation\.
+ The stack import operation supports creating a stack set with self\-managed permissions\.
+ The StackSets quotas and stack instances apply when importing stacks\. For more information about quotas, see [AWS CloudFormation quotas](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/cloudformation-limits.html)\.

## Importing a stack into a stack set \(console\)<a name="importing-stack-to-stackset"></a>

### Import a stack into a new stack set<a name="import-stack-to-stackset"></a>

Import a stack into a new stack set using the AWS Management Console

To import an existing stack into a stack set, identify a stack that contains the resource you want to import\.

1. Sign in to the AWS Management Console and open the AWS CloudFormation console at [https://console\.aws\.amazon\.com/cloudformation](https://console.aws.amazon.com/cloudformation/)\.

1. From the navigation pane, choose **StackSets**\.

1. At the top of the **StackSets** page, choose **Create StackSet**\.

1. On the **Choose a template** page, specify a template by one of the following options and select **Next**\.
   + Choose **Amazon S3 URL** and specify the URL for your template in the text box\.
   + Choose **Upload a template file** and browse for your template\.
   + Choose **From stack ID** and enter your stack ID\.

1. On the **Specify StackSet details** page, enter the name of a stack set you want to create and select **Next**\.

   \(Optional\) Enter a description of the stack set\.

1. On the **Configure StackSet options** page, review your choices and select **Next**\.

1. On the **Set deployment options** page, select **Import stacks to stack set**\.

1. Enter the stack ID of the stack you want to import in the **Stacks to import** field\. For example, `arn:123456789101:us-east-1:StackToImport`\.

   \(Optional\) Select **Add another stack ID** and enter the stack ID of another stack you want to import\. You may add up to 10 stacks per stack import operation\.

1. Review your deployment options and select **Next**\.

1. On the **Review** page, review your choices and your stack set's properties\. When you are ready to import your stack into your stack set, select **Submit**\.

**Results**: The imported stack is now a stack instance of the specified stack set\. To learn more about the stack import status, see [Stack set and stack instance status codes](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/stacksets-concepts.html#stackset-status-codes)\.

### Import a stack into an existing stack set<a name="import-stack-to-existing-stackset"></a>

Import a stack into an existing stack set using the AWS Management Console

To import an existing stack into a stack set, identify a stack that contains the resource you want to import\.

1. Sign in to the AWS Management Console and open the AWS CloudFormation console at [https://console\.aws\.amazon\.com/cloudformation](https://console.aws.amazon.com/cloudformation/)\.

1. From the navigation pane, choose **StackSets**\.

1. On the **StackSets** page, select the stack set that you want to import a stack into\.

1. With the stack set selected, choose **Add stacks to StackSet** from the **Actions** menu\.

1. On the **Set deployment options** page, select **Import stacks to stack set** and enter the stack ID of the stack you want to import in the **Stacks to import** field\. For example, `arn:123456789101:us-east-1:StackToImport`\.

   \(Optional\) Select **Add another stack ID** and enter the stack ID of another stack you want to import\. You may add up to 10 stacks per stack import operation\.

1. Choose **Next**\.

1. On the **Specify overrides** page, review your choices and select **Next**\.

1. On the **Review** page, review your choices and your stack set's properties\. When you are ready to create your stack set, choose **Submit**\.

**Results**: The imported stack is now a stack instance of the specified stack set\. To learn more about the stack import status, see [Stack set and stack instance status codes](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/stacksets-concepts.html#stackset-status-codes)\.

## Importing a stack into a stack set \(AWS CLI\)<a name="importing-stack-to-stackset.cli"></a>

### Import a stack into a stack set<a name="import-stack-to-stackset-cli"></a>

To import an existing stack into a stack set, identify a stack that contains the resources you want to import\. In this example, the stack to import is `arn:123456789101:us-east-1:StackToImport`\.

1. Create a stack set from a stack ID\.

   ```
   create-stackset --stack-id "arn:123456789101:us-east-1:StackToImport" --stackSetName "SingleStackSetName" --permission-model "SELF_MANAGED" --administration-role-arn "AdminRole" --execution-role-name "ExecutionRole"
   ```

1. Import a specified stack to your stack set\.

   ```
   import-stack-to-stackset --stack-ids "arn:123456789101:us-east-1:StackToImport" --stackSet "SingleStackSetName" --mutate --permission-model SELF_MANAGED --administration-role-arn "AdminRole" --execution-role-name "ExecutionRole"
   ```

1. Clone the imported stack into other Regions and accounts\.

   ```
   create-stack-instances --stack-set-name "StackSetToWhichStackimported" --accounts "123556789101" --regions "us-east-1"
   ```

### Import stacks into a stack set<a name="import-stacks-to-stackset-cli"></a>

To import existing stacks into a stack set, identify the stacks that contains the resources you want to import\. In this example, the stack to import is `arn:123456789101:us-east-1:StackToImport1` and `arn:123456789101:us-east-1:StackToImport2`\.

1. Create a stack set from a stack ID\.

   ```
   create-stackset --stack-id "arn:123456789101:us-east-1:StackToImport" --stackSetName "StackSetName" --permission-model "SELF_MANAGED" --administration-role-arn "AdminRole" --execution-role-name "ExecutionRole"
   ```

1. Import specified stacks to your stack set\.

   ```
    import-stacks-to-stackset --stack-ids "arn:123456789101:us-east-1:StackToImport1, arn:123456789101:us-east-1:StackToImport2" --stackSet "StackSetName" --permission-model SELF_MANAGED --administration-role-arn "AdminRole" --execution-role-name "ExecutionRole"
   ```

1. Clone the imported stack into other Regions and accounts\.

   ```
   create-stack-instances --stack-set-name "StackSetName" --accounts "123456789012" --regions "us-east-1"
   ```

## Reverting a stack import operation<a name="reverting-stackset-import"></a>

To revert a stack import operation, complete the following tasks:

1. Specify a `DeletionPolicy` attribute of `Retain` for each resource that you want to keep after the stack instance is deleted\. For more information, see [Reverting an import operation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/resource-import-revert.html)\.

1. Delete stack instances from your stack set\. For more information, see [Delete stack instances from your stack set](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/stackinstances-delete.html)\.

1. Delete your stack set\. For more information, see [Delete a stack set](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/stacksets-delete.html)\.

**Results**: The revert operation has deleted the stack instance and retained the stack's resources\.