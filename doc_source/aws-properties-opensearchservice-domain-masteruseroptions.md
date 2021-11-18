# AWS::OpenSearchService::Domain MasterUserOptions<a name="aws-properties-opensearchservice-domain-masteruseroptions"></a>

Specifies information about the master user\.

## Syntax<a name="aws-properties-opensearchservice-domain-masteruseroptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-opensearchservice-domain-masteruseroptions-syntax.json"></a>

```
{
  "[MasterUserARN](#cfn-opensearchservice-domain-masteruseroptions-masteruserarn)" : String,
  "[MasterUserName](#cfn-opensearchservice-domain-masteruseroptions-masterusername)" : String,
  "[MasterUserPassword](#cfn-opensearchservice-domain-masteruseroptions-masteruserpassword)" : String
}
```

### YAML<a name="aws-properties-opensearchservice-domain-masteruseroptions-syntax.yaml"></a>

```
  [MasterUserARN](#cfn-opensearchservice-domain-masteruseroptions-masteruserarn): String
  [MasterUserName](#cfn-opensearchservice-domain-masteruseroptions-masterusername): String
  [MasterUserPassword](#cfn-opensearchservice-domain-masteruseroptions-masteruserpassword): String
```

## Properties<a name="aws-properties-opensearchservice-domain-masteruseroptions-properties"></a>

`MasterUserARN`  <a name="cfn-opensearchservice-domain-masteruseroptions-masteruserarn"></a>
ARN for the master user\. Only specify if `InternalUserDatabaseEnabled` is false in `AdvancedSecurityOptions`\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`MasterUserName`  <a name="cfn-opensearchservice-domain-masteruseroptions-masterusername"></a>
Username for the master user\. Only specify if `InternalUserDatabaseEnabled` is true in `AdvancedSecurityOptions`\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`MasterUserPassword`  <a name="cfn-opensearchservice-domain-masteruseroptions-masteruserpassword"></a>
Password for the master user\. Only specify if `InternalUserDatabaseEnabled` is true in `AdvancedSecurityOptions`\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)