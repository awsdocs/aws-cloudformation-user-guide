# Reviewing your stack on the AWS CloudFormation console<a name="cfn-using-console-create-stack-review"></a>

The final step before your stack is launched is to review the values entered while creating the stack\.

1. On the **Review** page, review the details of your stack\.

   If you need to change any of the values before launching the stack, choose **Edit** on the appropriate section to go back to the page that has the setting that you want to change\.

1. After you review the stack creation settings, choose **Create stack** to launch your stack\.
**Note**  
As this point, you can also choose to create a new change set rather than a new stack\. To do so, click **Create change set** instead of **Create stack**\. For more information, see [Creating stacks using change sets](cfn-console-create-stacks-changesets.md)

   CloudFormation displays the **Events** pane of the **Stack details** page for your new stack\. From here, you can [view your stack's events, data, or resources](cfn-console-view-stack-data-resources.md)\. CloudFormation automatically refreshes the stack events every minute\. Additionally, CloudFormation displays the **New events available** badge when new stack events occur; choose the refresh icon to load these events into the list\. By viewing stack creation events, you can understand the sequence of events that lead to your stack's creation \(or failure, if you are debugging your stack\)\.

   While your stack is being created, it's listed on the **Stacks** page with a status of **CREATE\_IN\_PROGRESS**\.

   After your stack has been successfully created, its status changes to **CREATE\_COMPLETE**\. You can then choose the **Outputs** tab to view your stack's outputs if you have defined any in the template\.