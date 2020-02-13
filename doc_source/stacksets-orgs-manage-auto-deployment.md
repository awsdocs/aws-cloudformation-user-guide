# Manage Automatic Deployments for a Stack Set with Service\-Managed Permissions<a name="stacksets-orgs-manage-auto-deployment"></a>

With automatic deployment enabled, StackSets automatically deploys to accounts that are added to the target organization or organizational units \(OUs\) in the future\. With retain stacks enabled, when an account is removed from a target OU, stack resources in the account are retained\. You can adjust the automatic deployment settings you specified when you created your stack set at any time\.

**Topics**
+ [Manage Automatic Deployments Using the AWS CloudFormation Console](#stacksets-orgs-manage-auto-deployment-console)
+ [Manage Automatic Deployments Using the AWS CLI](#stacksets-orgs-manage-auto-deployment-cli)
+ [Auto Deployment Example](#stacksets-orgs-auto-deployment-example)

## Manage Automatic Deployments Using the AWS CloudFormation Console<a name="stacksets-orgs-manage-auto-deployment-console"></a>

1. Open the AWS CloudFormation console at [https://console.aws.amazon.com/cloudformation.](https://console.aws.amazon.com/cloudformation.)

1. From the navigation pane, choose **StackSets**\.

1. On the **StackSets** page, select the stack set that you created in [Creating a Stack Set with Service\-Managed Permissions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/stacksets-orgs-associate-stackset-with-org.html)\.

1. With the stack set selected, choose **Edit automatic deployment** from the **Actions** menu\. Automatic deployment is set at the stack set level\. You cannot adjust automatic deployments selectively for OUs, accounts, or Regions\.  
![\[Select stack set and choose Edit automatic deployment from the Actions menu.\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/console-stackset-edit-auto-deploy.png)

1. In the **Edit automatic deployment** modal, manage **Automatic deployment** and **Account removal behavior** settings\.  
![\[Edit automatic deployments modal.\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/console-stackset-edit-auto-deploy-modal.png)
**Note**  
With **Retain stacks** selected, stack instances are removed from your stack set, but the stacks and their associated resources are retained\. The resources stay in their current state, but are no longer part of the stack set\. The stacks cannot be reassociated with an existing or new stack set\.

1. Choose **Save**\.

## Manage Automatic Deployments Using the AWS CLI<a name="stacksets-orgs-manage-auto-deployment-cli"></a>

1. Open the AWS CLI\.

1. Run the `update-stack-set` command, specifying the the stack set that you created in [Creating a Stack Set with Service\-Managed Permissions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/stacksets-orgs-associate-stackset-with-org.html)\. Automatic deployment is set at the stack set level\. If you specify *\-\-auto\-deployment* in your stack set update, you cannot specify *\-\-deployment\-targets* or *\-\-regions*\.

   ```
   aws cloudformation update-stack-set --stack-set-name StackSet_myApp --auto-deployment Enabled=false
   ```

1. Using the `operation-id` that was returned as part of the `update-stack-set` output in step 2, run `describe-stack-set-operation` to verify that your stack set was updated successfully\.

   ```
   aws cloudformation describe-stack-set-operation --operation-id operation_ID
   ```

## Auto Deployment Example<a name="stacksets-orgs-auto-deployment-example"></a>

With automatic deployments enabled, automatic deployments are triggered when accounts are added to a target organization or OU, removed from a target organization or OU, or moved between target OUs\.

For example, a stack set `StackSet1` targets the OU `OU1` in the `us-east-1` region, and a stack set `StackSet2` targets the OU `OU2` in the `us-east-1` region\. `OU1` contains the account `AccountA`\.

If we move `AccountA` from `OU1` to `OU2` with automatic deployments enabled, StackSets automatically runs a delete operation to remove the `StackSet1` instance from `AccountA` and queues a create operation that will add the `StackSet2` instance to `AccountA`\. After the `StackSet1` instance is deleted, the `StackSet2` instance is created\.