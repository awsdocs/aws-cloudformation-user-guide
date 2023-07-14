# Amazon Verified Permissions resource type reference<a name="AWS_VerifiedPermissions"></a>

Amazon Verified Permissions is a permissions management service from AWS\. You can use Verified Permissions to manage permissions for your application, and authorize user access based on those permissions\. Using Verified Permissions, application developers can grant access based on information about the users, resources, and requested actions\. You can also evaluate additional information like group membership, attributes of the resources, and session context, such as time of request and IP addresses\. Verified Permissions manages these permissions by letting you create and store authorization policies for your applications, such as consumer\-facing web sites and enterprise business systems\.

Verified Permissions uses Cedar as the policy language to express your permission requirements\. Cedar supports both role\-based access control \(RBAC\) and attribute\-based access control \(ABAC\) authorization models\.

For more information about configuring, administering, and using Amazon Verified Permissions in your applications, see the [Amazon Verified Permissions User Guide](https://docs.aws.amazon.com/verified-permissions/latest/userguide)\.

For more information about the Cedar policy language, see the [Cedar Language Reference Guide](https://docs.cedarpolicy.com)\.

**Important**  
When you write Cedar policies that reference principals, resources and actions, you can define the unique identifiers used for each of those elements\. We strongly recommend that you follow these best practices:  
**Use values like universally unique identifiers \(UUIDs\) for all principal and resource identifiers\.**  
For example, if user `jane` leaves the company, and you later let someone else use the name `jane`, then that new user automatically gets access to everything granted by policies that still reference `User::"jane"`\. Cedar can't distinguish between the new user and the old\. This applies to both principal and resource identifiers\. Always use identifiers that are guaranteed unique and never reused to ensure that you don't unintentionally grant access because of the presence of an old identifier in a policy\.  
Where you use a UUID for an entity, we recommend that you follow it with the // comment specifier and the 'friendly' name of your entity\. This helps to make your policies easier to understand\. For example:  
`principal == User::"a1b2c3d4-e5f6-a1b2-c3d4-EXAMPLE11111", // alice`
**Do not include personally identifying, confidential, or sensitive information as part of the unique identifier for your principals or resources\.** These identifiers are included in log entries shared in AWS CloudTrail trails\.

**Resource types**
+ [AWS::VerifiedPermissions::IdentitySource](aws-resource-verifiedpermissions-identitysource.md)
+ [AWS::VerifiedPermissions::Policy](aws-resource-verifiedpermissions-policy.md)
+ [AWS::VerifiedPermissions::PolicyStore](aws-resource-verifiedpermissions-policystore.md)
+ [AWS::VerifiedPermissions::PolicyTemplate](aws-resource-verifiedpermissions-policytemplate.md)