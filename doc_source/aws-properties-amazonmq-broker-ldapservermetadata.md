# AWS::AmazonMQ::Broker LdapServerMetadata<a name="aws-properties-amazonmq-broker-ldapservermetadata"></a>

Optional\. The metadata of the LDAP server used to authenticate and authorize connections to the broker\.

**Important**  
Does not apply to RabbitMQ brokers\.

## Syntax<a name="aws-properties-amazonmq-broker-ldapservermetadata-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-amazonmq-broker-ldapservermetadata-syntax.json"></a>

```
{
  "[Hosts](#cfn-amazonmq-broker-ldapservermetadata-hosts)" : [ String, ... ],
  "[RoleBase](#cfn-amazonmq-broker-ldapservermetadata-rolebase)" : String,
  "[RoleName](#cfn-amazonmq-broker-ldapservermetadata-rolename)" : String,
  "[RoleSearchMatching](#cfn-amazonmq-broker-ldapservermetadata-rolesearchmatching)" : String,
  "[RoleSearchSubtree](#cfn-amazonmq-broker-ldapservermetadata-rolesearchsubtree)" : Boolean,
  "[ServiceAccountPassword](#cfn-amazonmq-broker-ldapservermetadata-serviceaccountpassword)" : String,
  "[ServiceAccountUsername](#cfn-amazonmq-broker-ldapservermetadata-serviceaccountusername)" : String,
  "[UserBase](#cfn-amazonmq-broker-ldapservermetadata-userbase)" : String,
  "[UserRoleName](#cfn-amazonmq-broker-ldapservermetadata-userrolename)" : String,
  "[UserSearchMatching](#cfn-amazonmq-broker-ldapservermetadata-usersearchmatching)" : String,
  "[UserSearchSubtree](#cfn-amazonmq-broker-ldapservermetadata-usersearchsubtree)" : Boolean
}
```

### YAML<a name="aws-properties-amazonmq-broker-ldapservermetadata-syntax.yaml"></a>

```
  [Hosts](#cfn-amazonmq-broker-ldapservermetadata-hosts): 
    - String
  [RoleBase](#cfn-amazonmq-broker-ldapservermetadata-rolebase): String
  [RoleName](#cfn-amazonmq-broker-ldapservermetadata-rolename): String
  [RoleSearchMatching](#cfn-amazonmq-broker-ldapservermetadata-rolesearchmatching): String
  [RoleSearchSubtree](#cfn-amazonmq-broker-ldapservermetadata-rolesearchsubtree): Boolean
  [ServiceAccountPassword](#cfn-amazonmq-broker-ldapservermetadata-serviceaccountpassword): String
  [ServiceAccountUsername](#cfn-amazonmq-broker-ldapservermetadata-serviceaccountusername): String
  [UserBase](#cfn-amazonmq-broker-ldapservermetadata-userbase): String
  [UserRoleName](#cfn-amazonmq-broker-ldapservermetadata-userrolename): String
  [UserSearchMatching](#cfn-amazonmq-broker-ldapservermetadata-usersearchmatching): String
  [UserSearchSubtree](#cfn-amazonmq-broker-ldapservermetadata-usersearchsubtree): Boolean
```

## Properties<a name="aws-properties-amazonmq-broker-ldapservermetadata-properties"></a>

`Hosts`  <a name="cfn-amazonmq-broker-ldapservermetadata-hosts"></a>
Specifies the location of the LDAP server such as AWS Directory Service for Microsoft Active Directory\. Optional failover server\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleBase`  <a name="cfn-amazonmq-broker-ldapservermetadata-rolebase"></a>
 The distinguished name of the node in the directory information tree \(DIT\) to search for roles or groups\. For example, `ou=group`, `ou=corp`, `dc=corp`, `dc=example`, `dc=com`\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleName`  <a name="cfn-amazonmq-broker-ldapservermetadata-rolename"></a>
Specifies the LDAP attribute that identifies the group name attribute in the object returned from the group membership query\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleSearchMatching`  <a name="cfn-amazonmq-broker-ldapservermetadata-rolesearchmatching"></a>
The LDAP search filter used to find roles within the roleBase\. The distinguished name of the user matched by userSearchMatching is substituted into the `{0}` placeholder in the search filter\. The client's username is substituted into the `{1}` placeholder\. For example, if you set this option to `(member=uid={1})` for the user janedoe, the search filter becomes `(member=uid=janedoe)` after string substitution\. It matches all role entries that have a member attribute equal to `uid=janedoe` under the subtree selected by the `RoleBases`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleSearchSubtree`  <a name="cfn-amazonmq-broker-ldapservermetadata-rolesearchsubtree"></a>
 The directory search scope for the role\. If set to true, scope is to search the entire subtree\.   
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ServiceAccountPassword`  <a name="cfn-amazonmq-broker-ldapservermetadata-serviceaccountpassword"></a>
 Service account password\. A service account is an account in your LDAP server that has access to initiate a connection\. For example, `cn=admin`,`dc=corp`, `dc=example`, `dc=com`\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ServiceAccountUsername`  <a name="cfn-amazonmq-broker-ldapservermetadata-serviceaccountusername"></a>
Service account username\. A service account is an account in your LDAP server that has access to initiate a connection\. For example, cn=admin,dc=corp, dc=example, dc=com\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UserBase`  <a name="cfn-amazonmq-broker-ldapservermetadata-userbase"></a>
Select a particular subtree of the directory information tree \(DIT\) to search for user entries\. The subtree is specified by a DN, which specifies the base node of the subtree\. For example, by setting this option to `ou=Users`,`ou=corp`, `dc=corp`, `dc=example`, `dc=com`, the search for user entries is restricted to the subtree beneath `ou=Users`,`ou=corp`, `dc=corp`, `dc=example`, `dc=com`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UserRoleName`  <a name="cfn-amazonmq-broker-ldapservermetadata-userrolename"></a>
Specifies the name of the LDAP attribute for the user group membership\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UserSearchMatching`  <a name="cfn-amazonmq-broker-ldapservermetadata-usersearchmatching"></a>
The LDAP search filter used to find users within the `userBase`\. The client's username is substituted into the `{0}` placeholder in the search filter\. For example, if this option is set to `(uid={0})` and the received username is `janedoe`, the search filter becomes `(uid=janedoe)` after string substitution\. It will result in matching an entry like `uid=janedoe`, `ou=Users`, `ou=corp`, `dc=corp`, `dc=example`, `dc=com`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UserSearchSubtree`  <a name="cfn-amazonmq-broker-ldapservermetadata-usersearchsubtree"></a>
The directory search scope for the user\. If set to true, scope is to search the entire subtree\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)