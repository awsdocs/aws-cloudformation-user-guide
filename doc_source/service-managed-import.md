# Service\-managed stack import for AWS CloudFormation StackSets<a name="service-managed-import"></a>

The AWS CloudFormation stack import operation can import existing stacks into new or existing stack sets, so that you can migrate existing stacks to a stack set in one operation\. StackSets extends the functionality of stacks, so you can create, update, or delete stacks across multiple accounts and Regions with a single operation\.

## Service\-managed requirements for stack import<a name="stackset-import-considerations-service-managed"></a>

In addition to the [Requirements for stack import](stacksets-import.md#stackset-import-considerations) section, service\-managed stack imports requires the following\.
+ The stack import operation requires a management account or delegated admin account in which you can manage the associated AWS Organizations such as enabling trust access with StackSets\.
+ The target accounts are must be members of the AWS Organizations managed by the management account or delegated admin account\.
+ Target stack exits in one of the target OUs\.
+ The target account should be a member of AWS Organizations\.
+ AWS Organizations access should be in the `ENABLED` state for the Organizations\.
+ Stacks being imported should be present in any of the member accounts, and not the management account\.

## Import a service\-managed stack into a new stack set \(console\)<a name="import-service-managed-stack-to-new-stackset"></a>

Import a stack into a new stack set using the AWS Management Console

To import a new stack into a stack set, identify a stack that contains the resource you want to import\.

1. Sign in to the AWS Management Console and open the AWS CloudFormation console at [https://console\.aws\.amazon\.com/cloudformation](https://console.aws.amazon.com/cloudformation/)\.

1. From the navigation pane, choose **StackSets**\.

1. At the top of the **StackSets** page, choose **Create StackSet**\.

1. Add the following information to the **Choose a template** page\.

   1. For **StackSet permission model** select **Service\-managed permissions**\.

   1. For **Prerequisite \- Prepare template**, select **Template is ready**\.

      1. For **Amazon S3 URL**, enter your Amazon S3 URL in the **Amazon S3 URL** field\.

      1. For **Upload a template file**, select a CloudFormation template on your local computer\.

   Accept your settings and choose **Next**\.

1. Add the following information to the **Specify StackSet details** page\.

   1. Enter a stack set name in the **StackSet name** box\.

   1. \(Optional\) Enter a description in the **StackSet description** section\.

   On the **Configure StackSet options** page, review your choices and select **Next**\.

1. Add the following information to the **Set deployment options** page\.

   1. For **Add stacks to stack set**, select **Import stacks to stack set**\.

   1. For **Stacks to import**, choose your stack import method\.

      1. For **Stack ID** enter your stack ID\.

      1. For **Stack URL** enter the Amazon S3 URL\.

1. Add the following information to the **Associate organizational units** section\.

   1. Select **Associate with organization** to use root OU\.

   1. Select **Associate with organizational units \(OUs\)** to enter parent OU IDs for the stacks to import\. For example, if `Stack 1` and `Stack 2` are under `OU1`, and `Stack 3` is under `OU2`, enter `OU1` and `OU2`\.

   Accept your settings and choose **Next**\.

1. Review your settings on the **Review** page and choose **Submit**\.

## Create and import a service\-managed stack into an existing stack set \(console\)<a name="import-service-managed-stack-to-existing-stackset"></a>

To import an existing stack into a new stack set, identify a stack that contains the resource you want to import\.

**To create a stack set and import a stack**

1. Sign in to the AWS Management Console and open the AWS CloudFormation console at [https://console\.aws\.amazon\.com/cloudformation](https://console.aws.amazon.com/cloudformation/)\.

1. From the navigation pane, choose **StackSets**\.

1. At the top of the **StackSets** page, choose **Create StackSet**\.

1. Add the following information to the **Choose a template** page\.

   1. For **StackSet permission model** select **Service\-managed permissions**\.

   1. For **Prerequisite \- Prepare template**, select **Template is ready**\.

      1. For **Amazon S3 URL**, enter your Amazon S3 URL in the **Amazon S3 URL** field\.

      1. For **Upload a template file**, select a CloudFormation template on your local computer\.

   Accept your settings and choose **Next**\.

1. Add the following information to the **Specify StackSet details** page\.

   1. Enter a stack set name in the **StackSet name** box\.

   1. \(Optional\) Enter a description in the **StackSet description** section\.

   On the **Configure StackSet options** page, review your choices and select **Next**\.

1. Add the following information to the **Set deployment options** page\.

   1. For **Add stacks to stack set**, select **Deploy new stacks**\.

1. Add the following information to the **Associate organizational units** section\.

   1. Select **Associate with organization** to use root OU\.

   1. Select **Associate with organizational units \(OUs\)** to enter parent OU IDs for the stacks to import\. For example, if `Stack 1` and `Stack 2` are under `OU1`, and `Stack 3` is under `OU2`, enter `OU1` and `OU2`\.

1. For **Specify regions** and **Deployment options**, review your choices\.

   Accept your settings and choose **Next**\.

1. Review your settings on the **Review** page and choose **Submit**\.

## Import a service\-managed stack into an existing stack set \(console\)<a name="import-service-managed-stack-to-existing-stackset-console"></a>

Select your stack set and identify the stack you want to import\.

**To import a stack to an existing stack set**

1. Sign in to the AWS Management Console and open the AWS CloudFormation console at [https://console\.aws\.amazon\.com/cloudformation](https://console.aws.amazon.com/cloudformation/)\.

1. From the navigation pane, choose **StackSets**\.

1. Select the stack set you want to import a stack to, and then choose **Add stacks to StackSet** from the **Actions** drop\-down\.

1. Add the following information to the **Set deployment options** page\.

   1. For **Add stacks to stack set**, select **Import stacks to stack set**\.

   1. Add the following information to the **Stacks to import** section\.

      1. For **Stack ID**, enter your stack ID\.

      1. For **Stack URL**, enter the Amazon S3 URL\.

   1. Add the following information to the **Associate organizational units** section\.

      1. Select **Associate with organization** to use root OU\.

      1. Select **Associate with organizational units \(OUs\)** to enter parent OU IDs for the stacks to import\. For example, if `Stack 1` and `Stack 2` are under `OU1`, and `Stack 3` is under `OU2`, enter `OU1` and `OU2`\.

      Accept your settings and choose **Next**\.

1. Review the **Specify overrides** page and choose **Next**\.

1. Confirm and review the **Review** page and choose **Submit**\.

## Importing a service\-managed stack into a stack set \(AWS CLI\)<a name="import-service-managed-stack-to-stackset.cli"></a>

Once a stack set is created, you can import your stacks by passing the stack ID's of the stacks being imported\. You may also pass the OU ID list to which you want to map it to\.

StackSets will import user provided stacks within those OUs and use those OUs as deployment targets for the stack sets\. Stack IDs presented in the input will map to the nearest OU in OU ID list input internally\. If a stack doesn't belong to an existing OU ID in the input list, then the AWS CLI will return the `StackNotFoundException` error\.

The `import-stacks-to-stack-set` operation creates stack instances for the stacks in the OU ID input\. The following AWS CLI examples use the `import-stacks-to-stack-set` operation to import a stack into a stack set\.
+ To use the `import-stacks-to-stack-sets` operation, specify `stack-ids` or `stack-ids-url` you want to import to your stack set\.

  ```
  aws cloudformation import-stacks-to-stack-set \
    --stack-set-name ServiceMangedStackSet \
    --stack-ids "arn:123456789012:us-east-1:Stack1" \
    --organizational-unit-ids ou-examplerootid111-exampleouid111
  ```

  ```
  aws cloudformation import-stacks-to-stack-set \
    --stack-set-name ServiceMangedStackSet \
    --stack-ids-url https://DOC-EXAMPLE-BUCKET \
    --organizational-unit-ids ou-examplerootid111-exampleouid111
  ```

**Note**  
The `import-stacks-to-stack-sets` operation, requires you to specify at least one organizational unit ID \(OU ID\) so that it can associate the stack being imported to that particular OU\. This operation doesn't create stack instances for other member accounts in the associated OUs\. To update member accounts for the associated OUs, use `create-stack-instances` or `update-stack-instances`\.

`create-stack-set` creates stack instances for all the accounts under the OUs with a user provided template, either from direct upload or Amazon S3\. The following AWS CLI examples use the `create-stack-set` operation to import a stack into a new stack set\.
+ To use the `create-stack-set` operation, specify your stack set name and import a stack to a newly created stack set\.

  ```
  aws cloudformation create-stack-set \
    --template-url https://DOC-EXAMPLE-BUCKET \
    --permission-model SERVICE_MANAGED \
    --auto-deployment Enabled=true
  ```