# Estimating the cost of your CloudFormation stack<a name="using-cfn-paying"></a>

There is no additional charge for AWS CloudFormation\. You pay for AWS resources \(e\.g\. Amazon EC2 instances, Elastic Load Balancing load balancers and so on\) created using AWS CloudFormation as if you created them by hand\.

**To estimate the cost of your stack**

1. On the **Review** page of the **Create stack** wizard, in the **Template** section, click the **Estimate cost** link\.  
![\[The Cost link on the Review page.\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/console-create-stack-review-template-cost.png)

   This link opens the **AWS Simple Monthly Calculator** in a new browser tab\.
**Note**  
Because you launched the calculator from the AWS CloudFormation console, it is pre\-populated with your template configuration and parameter values\. There are many additional configurable values that can provide you with a better estimate if you have an idea of how much data transfer you expect to your Amazon EC2 instance\. 

1. Click the **Estimate of your Monthly Bill** tab for a monthly estimate of running your stack, along with a categorized display of what factors contributed to the estimate\.