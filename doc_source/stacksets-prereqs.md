# Prerequisites for stack set operations<a name="stacksets-prereqs"></a>

Because stack sets perform stack operations across multiple accounts, before you can create your first stack set you need the necessary permissions defined in your AWS accounts\.

To set up the required permissions for creating a stack set with **self\-managed** permissions, see [Performing stack set operations involving regions that are disabled by default](#stacksets-opt-in-regions) and [Grant self\-managed permissions](stacksets-prereqs-self-managed.md)\.

To set up the required permissions for creating a stack set with **service\-managed** permissions, see [Performing stack set operations involving regions that are disabled by default](#stacksets-opt-in-regions) and [Enable trusted access with AWS Organizations](stacksets-orgs-enable-trusted-access.md)\.

## Performing stack set operations involving regions that are disabled by default<a name="stacksets-opt-in-regions"></a>

AWS Regions introduced after March 20, 2019, such as Asia Pacific \(Hong Kong\), are disabled by default\. You must enable these Regions for your account\(s\) before you can use them\. Because of this, consider the following before performing stack set operations involving accounts in Regions that are disabled by default:
+ To create a stack set from a stack set's administrator account \(if using self\-managed permissions\) or organization's management account \(if using service\-managed permissions\) in a Region that is disabled by default, you must first enable that Region for the administrator or management account\.
+ For AWS CloudFormation to successfully create or update a stack instance:
  + The target account must reside in a Region that is currently enabled for that target account\.
  + The stack set's administrator account or organization's management account must have the same Region enabled as the target account\.

**Important**  
Be aware that during stack set operations, administrator and target accounts exchange metadata regarding the accounts themselves, as well as the stack set and stack set instances involved\.  
In addition, if you disable a Region that contains an account in which stack set instances reside, you are responsible for deleting any such instances or resources, if desired\. In addition, be aware that metadata regarding the target account in the disabled Region will be retained in the administrator account\.

For more information about enabling and disabling regions, see [Managing AWS Regions](https://docs.aws.amazon.com/general/latest/gr/rande-manage.html) in the *AWS General Reference*\.

**Topics**
+ [Performing stack set operations involving regions that are disabled by default](#stacksets-opt-in-regions)
+ [Grant self\-managed permissions](stacksets-prereqs-self-managed.md)
+ [Enable trusted access with AWS Organizations](stacksets-orgs-enable-trusted-access.md)