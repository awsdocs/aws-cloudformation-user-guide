# What is AWS CloudFormation?<a name="Welcome"></a>

AWS CloudFormation is a service that helps you model and set up your Amazon Web Services resources so that you can spend less time managing those resources and more time focusing on your applications that run in AWS\. You create a template that describes all the AWS resources that you want \(like Amazon EC2 instances or Amazon RDS DB instances\), and AWS CloudFormation takes care of provisioning and configuring those resources for you\. You don't need to individually create and configure AWS resources and figure out what's dependent on what; AWS CloudFormation handles all of that\. The following scenarios demonstrate how AWS CloudFormation can help\.

## Simplify infrastructure management<a name="w7739ab1b5b5"></a>

For a scalable web application that also includes a back\-end database, you might use an Auto Scaling group, an Elastic Load Balancing load balancer, and an Amazon Relational Database Service database instance\. Normally, you might use each individual service to provision these resources\. And after you create the resources, you would have to configure them to work together\. All these tasks can add complexity and time before you even get your application up and running\.

Instead, you can create or modify an existing AWS CloudFormation template\. A template describes all of your resources and their properties\. When you use that template to create an AWS CloudFormation stack, AWS CloudFormation provisions the Auto Scaling group, load balancer, and database for you\. After the stack has been successfully created, your AWS resources are up and running\. You can delete the stack just as easily, which deletes all the resources in the stack\. By using AWS CloudFormation, you easily manage a collection of resources as a single unit\.

## Quickly replicate your infrastructure<a name="w7739ab1b5b7"></a>

If your application requires additional availability, you might replicate it in multiple regions so that if one region becomes unavailable, your users can still use your application in other regions\. The challenge in replicating your application is that it also requires you to replicate your resources\. Not only do you need to record all the resources that your application requires, but you must also provision and configure those resources in each region\.

When you use AWS CloudFormation, you can reuse your template to set up your resources consistently and repeatedly\. Just describe your resources once and then provision the same resources over and over in multiple regions\. 

## Easily control and track changes to your infrastructure<a name="w7739ab1b5b9"></a>

In some cases, you might have underlying resources that you want to upgrade incrementally\. For example, you might change to a higher performing instance type in your Auto Scaling launch configuration so that you can reduce the maximum number of instances in your Auto Scaling group\. If problems occur after you complete the update, you might need to roll back your infrastructure to the original settings\. To do this manually, you not only have to remember which resources were changed, you also have to know what the original settings were\.

When you provision your infrastructure with AWS CloudFormation, the AWS CloudFormation template describes exactly what resources are provisioned and their settings\. Because these templates are text files, you simply track differences in your templates to track changes to your infrastructure, similar to the way developers control revisions to source code\. For example, you can use a version control system with your templates so that you know exactly what changes were made, who made them, and when\. If at any point you need to reverse changes to your infrastructure, you can use a previous version of your template\.

## Related information<a name="w7739ab1b5c13"></a>
+ For more information about AWS CloudFormation stacks and templates, see [AWS CloudFormation concepts](cfn-whatis-concepts.md)\.
+ For an overview about how to use AWS CloudFormation, see [How does AWS CloudFormation work?](cfn-whatis-howdoesitwork.md)\.
+ For pricing information, see [AWS CloudFormation pricing](http://aws.amazon.com/cloudformation/pricing/)\.