# Self\-managed stack import for AWS CloudFormation StackSets<a name="self-managed-import"></a>

The AWS CloudFormation stack import operation can import existing stacks into new or existing stack sets, so that you can migrate existing stacks to a stack set in one operation\. StackSets extends the functionality of stacks, so you can create, update, or delete stacks across multiple accounts and Regions with a single operation\.

For example, if you have a stack that specifies an administrator AWS Identity and Access Management \(IAM\) role across multiple accounts, you can import that stack into a stack set\. By using stack import, you avoid downtime and outages without deleting and recreating those resources\. Once the stack is imported into a stack set, the original stack will become a stack instance of the newly generated stack set\.

## Self\-managed requirements for stack import<a name="self-managed-requirements-for-stack-import"></a>

In addition to the [Requirements for stack import](stacksets-import.md#stackset-import-considerations) section, self\-managed stack imports requires the following\.
+ The stack import operation supports creating a stack set with self\-managed permissions\.
+ The stack import operation requires an administrator account in which you create a stack set and a target account that contains a stack\.
+ The target account must have permission to use the `GetTemplate` operation with the input of stack ID or ARN\. Because of that, your administrator account must be granted **AWSCloudFormationStackSetsAdminstration** or **AWSCloudFormationStackSetsExectionRole** permissions\.

## Import a stack into a new stack set<a name="import-stacks-to-stack-set"></a>

Import a stack into a new stack set using the AWS Management Console

To import a stack into a stack set, identify a stack that contains the resource you want to import\.

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

## Import a self\-managed stack into an existing stack set<a name="import-stack-to-existing-stackset"></a>

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

### Import a stack into a stack set<a name="import-stacks-to-stack-set-cli"></a>

To import an existing stack into a stack set, identify a stack that contains the resources you want to import\. In this example, the stack to import is `arn:123456789101:us-east-1:StackToImport`\.

1. Create a stack set from a stack ID by specifying the full ARN of the CloudFormation stack to be imported\.\.

   ```
   aws cloudformation create-stack-set \
     --stack-id "arn:aws:cloudformation:us-east-1:123456789012:stack/StackToImport/f449b250-b969-11e0-a185-5081d0136786" \
     --stack-set-name "SingleStackSetName" \
     --permission-model "SELF_MANAGED" \
     --administration-role-arn "arn:aws:iam::123456789012:role/AWSCloudFormationStackSetAdministrationRole" \
     --execution-role-name "AWSCloudFormationStackSetExecutionRole"
   ```

1. Import a specified stack to your stack set\.

   ```
   aws cloudformation import-stacks-to-stack-set \
     --stack-ids "arn:aws:cloudformation:us-east-1:123456789012:stack/StackToImport/f449b250-b969-11e0-a185-5081d0136786" \
     --stack-set "SingleStackSetName" \
     --permission-model SELF_MANAGED \
     --administration-role-arn "arn:aws:iam::123456789012:role/AWSCloudFormationStackSetAdministrationRole" \
     --execution-role-name "AWSCloudFormationStackSetExecutionRole"
   ```

1. Clone the imported stack into other Regions and accounts\.

   ```
   aws cloudformation create-stack-instances \
     --stack-set-name "StackSetToWhichStackimported" \
     --accounts "123556789101" \
     --regions "us-east-1"
   ```

### Import stacks into a stack set<a name="import-stacks-to-stackset-cli"></a>

To import existing stacks into a stack set, identify the stacks that contains the resources you want to import\. In this example, the stack to import is `arn:aws:cloudformation:123456789101:us-east-1:stack/StackToImport1/f449b250-b969-11e0-a185-5081d0136786` and `arn:aws:cloudformation:123456789101:us-east-1:stack/StackToImport2/f449b250-b969-11e0-a185-5081d0136786`\.

1. Create a stack set from a stack ID\.

   ```
   aws cloudformation create-stack-set \
     --stack-id "arn:123456789101:us-east-1:StackToImport" \
     --stack-set-name "StackSetName" \
     --permission-model "SELF_MANAGED" \
     --administration-role-arn "arn:aws:iam::123456789012:role/AWSCloudFormationStackSetAdministrationRole" \
     --execution-role-name "AWSCloudFormationStackSetExecutionRole"
   ```

1. Import specified stacks to your stack set\.

   ```
   aws cloudformation import-stacks-to-stackset 
     --stack-ids "arn:aws:cloudformation:123456789101:us-east-1:stack/StackToImport1/f449b250-b969-11e0-a185-5081d0136786, arn:aws:cloudformation:123456789101:us-east-1:stack/StackToImport2/f449b250-b969-11e0-a185-5081d0136786" \
     --stack-set "StackSetName" 
     --permission-model SELF_MANAGED \
     --administration-role-arn "arn:aws:iam::123456789012:role/AWSCloudFormationStackSetAdministrationRole" \
     --execution-role-name "AWSCloudFormationStackSetExecutionRole"
   ```

1. Clone the imported stack into other Regions and accounts\.

   ```
   aws cloudformation create-stack-instances \
     --stack-set-name "StackSetName" \
     --accounts "123456789012" \
     --regions "us-east-1"
   ```