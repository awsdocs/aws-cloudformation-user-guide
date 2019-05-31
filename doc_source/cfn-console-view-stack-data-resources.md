# Viewing AWS CloudFormation Stack Data and Resources on the AWS Management Console<a name="cfn-console-view-stack-data-resources"></a>

## Viewing Stack Information<a name="w4784ab1c15c13c17b3"></a>

After you've created an AWS CloudFormation stack, you can use the AWS Management Console to view its data and resources\. You can view the following stack information:

**Outputs**  
Displays outputs that were declared in the stack's template\.

**Resources**  
Displays the resources that are part of the stack\.

**Events**  
Displays the operations that are tracked when you create, update, or delete the stack\.  
All events that are triggered by a given stack operation are assigned the same client request token, which you can use to track operations\. Stack operations that are initiated from the console use the token format *Console\-StackOperation\-ID*, which helps you to easily identify the stack operation\. For example, if you create a stack using the console, each resulting stack event would be assigned the same token in the following format: `Console-CreateStack-7f59c3cf-00d2-40c7-b2ff-e75db0987002`\. 

**Template**  
Displays the stack's template\.  
For stacks that contain transforms, choose **View original template** to view the user\-submitted template, or **View processed template** to view the template after AWS CloudFormation processes the transforms\. AWS CloudFormation uses the processed template to create or update your stack\.

**Parameters**  
Displays the stack's parameters and their values\.  
For stacks that contain `SSM` parameters, the **Resolved Value** column displays the values that are used in the stack definition for the `SSM` parameters\. For more information, see [SSM Parameter Types](parameters-section-structure.md#aws-ssm-parameter-types)\.

**Tags**  
Displays any tags that are associated with the stack\.

**Stack Policy**  
Describes the stack resources that are protected against stack updates\. For you to be able to update these resources, they must be explicitly allowed during a stack update\.

**To view information about your AWS CloudFormation stack**

1. Select your stack in the AWS CloudFormation console\. This displays information in the stack detail pane\.

1. In the detail pane, click a tab to view the related information about your stack\.

   For example, click **Outputs** to view the outputs that are associated with your stack\.  
![\[The Outputs tab in the detail pane.\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/console-stack-detail-pane.png)

## Stack Status Codes<a name="w4784ab1c15c13c17b5"></a>

The following table describes stack status codes:

### <a name="w4784ab1c15c13c17b5b4"></a>


| Stack Status | Description | 
| --- | --- | 
|  `CREATE_COMPLETE`  |  Successful creation of one or more stacks\.  | 
|  `CREATE_IN_PROGRESS`  |  Ongoing creation of one or more stacks\.  | 
|  `CREATE_FAILED`  |  Unsuccessful creation of one or more stacks\. View the stack events to see any associated error messages\. Possible reasons for a failed creation include insufficient permissions to work with all resources in the stack, parameter values rejected by an AWS service, or a timeout during resource creation\.  | 
|  `DELETE_COMPLETE`  |  Successful deletion of one or more stacks\. Deleted stacks are retained and viewable for 90 days\.  | 
|  `DELETE_FAILED`  |  Unsuccessful deletion of one or more stacks\. Because the delete failed, you might have some resources that are still running; however, you cannot work with or update the stack\. Delete the stack again or view the stack events to see any associated error messages\.  | 
|  `DELETE_IN_PROGRESS`  |  Ongoing removal of one or more stacks\.  | 
| REVIEW\_IN\_PROGRESS | Ongoing creation of one or more stacks with an expected StackId but without any templates or resources\. A stack with this status code counts against the [maximum possible number of stacks](cloudformation-limits.md)\.  | 
|  `ROLLBACK_COMPLETE`  |  Successful removal of one or more stacks after a failed stack creation or after an explicitly canceled stack creation\. Any resources that were created during the create stack action are deleted\. This status exists only after a failed stack creation\. It signifies that all operations from the partially created stack have been appropriately cleaned up\. When in this state, only a delete operation can be performed\.  | 
|  `ROLLBACK_FAILED`  |  Unsuccessful removal of one or more stacks after a failed stack creation or after an explicitly canceled stack creation\. Delete the stack or view the stack events to see any associated error messages\.  | 
|  `ROLLBACK_IN_PROGRESS`  |  Ongoing removal of one or more stacks after a failed stack creation or after an explicitly cancelled stack creation\.  | 
|  `UPDATE_COMPLETE`  | Successful update of one or more stacks\. | 
|  `UPDATE_COMPLETE_CLEANUP_IN_PROGRESS`  |  Ongoing removal of old resources for one or more stacks after a successful stack update\. For stack updates that require resources to be replaced, AWS CloudFormation creates the new resources first and then deletes the old resources to help reduce any interruptions with your stack\. In this state, the stack has been updated and is usable, but AWS CloudFormation is still deleting the old resources\.  | 
|  `UPDATE_IN_PROGRESS`  |  Ongoing update of one or more stacks\.  | 
|  `UPDATE_ROLLBACK_COMPLETE`  |  Successful return of one or more stacks to a previous working state after a failed stack update\.  | 
|  `UPDATE_ROLLBACK_COMPLETE_CLEANUP_IN_PROGRESS`  |  Ongoing removal of new resources for one or more stacks after a failed stack update\. In this state, the stack has been rolled back to its previous working state and is usable, but AWS CloudFormation is still deleting any new resources it created during the stack update\.  | 
|  `UPDATE_ROLLBACK_FAILED`  |  Unsuccessful return of one or more stacks to a previous working state after a failed stack update\. When in this state, you can delete the stack or [continue rollback](using-cfn-updating-stacks-continueupdaterollback.md)\. You might need to fix errors before your stack can return to a working state\. Or, you can contact customer support to restore the stack to a usable state\.  | 
|  `UPDATE_ROLLBACK_IN_PROGRESS`  |  Ongoing return of one or more stacks to the previous working state after failed stack update\.  | 