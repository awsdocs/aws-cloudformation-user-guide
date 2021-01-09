# Best practices<a name="stacksets-bestpractices"></a>

**Topics**
+ [Defining the template](#w7739ab1c29c23b6)
+ [Creating or adding stacks to the stack set](#w7739ab1c29c23b8)
+ [Updating stacks in a stack set](#w7739ab1c29c23c10)

Review the [AWS CloudFormation best practices](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/best-practices.html)\.

## Defining the template<a name="w7739ab1c29c23b6"></a>
+ Define the template that you want to standardize in multiple accounts, within multiple regions\.
+ As you create the template, be sure that global resources \(such as IAM roles and Amazon S3 buckets\) do not have naming conflicts when they are created in more than one region in the same account\.
+ A stack set has a single template and parameter set\. The same stack is created in all accounts that are associated with a stack set\. As you author your templates, make them granular enough to allow you a good balance of control and standardization\.  
+ We recommend that you store your template in an Amazon S3 bucket\.

## Creating or adding stacks to the stack set<a name="w7739ab1c29c23b8"></a>
+ Verify that adding stack instances to your initial stack set works before you add larger numbers of stack instances to your stack set\.
+ Choose the deployment \(rollout\) options that work for your use case\.
  + For a more conservative deployment, set **Maximum Concurrent Accounts** to 1, and **Failure Tolerance** to 0\. Set your lowest\-impact region to be first in the **Region Order** list\. Start with one region\.
  + For a faster deployment, increase the values of **Maximum Concurrent Accounts** and **Failure Tolerance** as needed\.
+ Operations on stack sets depend on how many stack instances are involved, and can take significant time\.

## Updating stacks in a stack set<a name="w7739ab1c29c23c10"></a>
+ By default, updating a stack set updates all stack instances\. If you have 20 accounts each in two regions, you will have 40 stack instances, and all will be updated when you update the stack set\.

  For stack sets with a large number of stack instances, we recommend that to test the updated version of a template, you selectively update the stack instances in a few test accounts before updating all stack instances\.
+ To get more granular control over updating individual stacks within your stack set, plan to create multiple stack sets\.
+ Updating a stack set that contains a large number of stacks can take significant time\. In this release, only one operation is permitted at a time on a stack set\. Plan your updates so you are not blocked from performing other operations on the stack set\.