# Reviewing Your Stack and Estimating Stack Cost on the AWS CloudFormation Console<a name="cfn-using-console-create-stack-review"></a>

The final step before your stack is launched is to review the values entered while creating the stack\. You can also estimate the cost of your stack\.

1. On the **Review** page, review the details of your stack\.

   If you need to change any of the values prior to launching the stack, click **Back** to go back to the page that has the setting that you want to change\.

1. \(Optional\) You can click the **Cost** link to estimate the cost of your stack\. The AWS Simple Monthly Calculator displays values from your stack template and launch settings\.

1. After you review the stack launch settings and the estimated cost of your stack, click **Create** to launch your stack\.

   Your stack appears in the list of AWS CloudFormation stacks, with a status of **CREATE\_IN\_PROGRESS**\.

   While your stack is being created \(or afterward\), you can use the stack detail pane to [view your stack's events, data, or resources](cfn-console-view-stack-data-resources.md)\. AWS CloudFormation automatically refreshes stack events every minute\. By viewing stack creation events, you can understand the sequence of events that lead to your stack's creation \(or failure, if you are debugging your stack\)\.

   After your stack has been successfully created, its status changes to **CREATE\_COMPLETE**\. You can then select it \(if necessary\) and click the **Outputs** tab to view your stack's outputs if you have defined any in the template\.