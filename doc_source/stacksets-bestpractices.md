# Best Practices<a name="stacksets-bestpractices"></a>

**Topics**
+ [Defining the Template](#w3ab2c19c19b6)
+ [Creating or Adding Stacks to the Stack Set](#w3ab2c19c19b8)
+ [Updating Stacks in a Stack Set](#w3ab2c19c19c10)

Review the [AWS CloudFormation Best Practices](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/best-practices.html)\.

## Defining the Template<a name="w3ab2c19c19b6"></a>
+ Define the template that you want to standardize in multiple accounts, within multiple regions\.
+ As you create the template, be sure that global resources \(such as IAM roles and Amazon S3 buckets\) do not have naming conflicts when they are created in more than one region in the same account\.
+ A stack set has a single template and parameter set\. The same stack is created in all accounts that are associated with a stack set\. As you author your templates, make them granular enough to allow you a good balance of control and standardization\. In this release, you cannot customize a stack per account or region unless the template has per account or per region configuration coded in it\.
+ We recommend that you store your template in an Amazon S3 bucket\.

## Creating or Adding Stacks to the Stack Set<a name="w3ab2c19c19b8"></a>
+ Verify that adding stack instances to your initial stack set works before you add larger numbers of stack instances to your stack set\.
+ Choose the deployment \(rollout\) options that work for your use case\.
  + For a more conservative deployment, set **Maximum Concurrent Accounts** to 1, and **Failure Tolerance** to 0\. Set your lowest\-impact region to be first in the **Region Order** list\. Start with one region\.
  + For a faster deployment, increase the values of **Maximum Concurrent Accounts** and **Failure Tolerance** as needed\.
+ Operations on stack sets depend on how many stack instances are involved, and can take significant time\.

## Updating Stacks in a Stack Set<a name="w3ab2c19c19c10"></a>
+ Updating a stack set always touches all stack instances\. If you have 20 accounts each in two regions, you will have 40 stack instances, and all will be updated when you update the stack set\.

  We recommend that to test the updated version of a template, you create a test stack set with the updated template, then add a few test accounts and deploy your template to the test stack set first\.
+ Because you cannot update only selected stacks within a stack set, to get more granular control over updating individual stacks within your stack set, plan to create multiple stack sets\.
+ Updating a stack set that contains a large number of stacks can take significant time\. In this release, only one operation is permitted at a time on a stack set\. Plan your updates so you are not blocked from performing other operations on the stack set\.