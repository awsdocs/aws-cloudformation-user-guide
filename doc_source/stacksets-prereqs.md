# Prerequisites for stack set operations<a name="stacksets-prereqs"></a>

Because stack sets perform stack operations across multiple accounts, before you can create your first stack set you need the necessary permissions defined in your AWS accounts\.

To set up the required permissions for creating a stack set with **self\-managed** permissions, see [Grant self\-managed permissions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/stacksets-prereqs-self-managed.html)\.

To set up the required permissions for creating a stack set with **service\-managed** permissions, see [Enable Trusted Access with AWS Organizations](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/stacksets-orgs-enable-trusted-access.html)\.

## Performing stack set operations involving accounts in opt\-in regions<a name="stacksets-opt-in-regions"></a>

AWS Regions introduced after March 20, 2019, such as Asia Pacific \(Hong Kong\), are disabled by default\. You must enable these Regions for your account\(s\) before you can use them\. Because of this, consider the following when performing stack set operations involving accounts in Regions that are disabled by default\. 
+ You cannot create a stack set from an administrator account in a Region that is currently disabled for that account\.
+ For CloudFormation to successfully create or update a stack instance, the target account must reside in a Region that is currently enabled for that account\.
+ To deploy stack instances into a target account that resides in a Region that is disabled by default, and that is enabled for the target account but *disabled* for the administrator account, the `AdministrationRole` needs to trust both global CloudFormation service principal, as well as the regional service principal\. 

**Important**  
Be aware that during stack set operations, adminstrator and target accounts exchange metadata regarding the accounts themselves, as well as the stack set and stack set instances involved\.  
In addition, if you disable a Region that contains an account in which stack set instances reside, you are responsible for deleting any such instances or resources, if desired\. In addition, be aware that metadata regarding the target account in the disabled Region will be retained in the administrator account\.

For more information on enabling and disabling regions, see [Managing AWS Regions](https://docs.aws.amazon.com/general/latest/gr/rande-manage.html) in the *AWS General Reference*\.

**Topics**
+ [Performing stack set operations involving accounts in opt\-in regions](#stacksets-opt-in-regions)
+ [Grant self\-managed permissions](stacksets-prereqs-self-managed.md)
+ [Enable trusted access with AWS Organizations](stacksets-orgs-enable-trusted-access.md)