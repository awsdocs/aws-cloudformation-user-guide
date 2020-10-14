# AWS::Elasticsearch::Domain MasterUserOptions<a name="aws-properties-elasticsearch-domain-masteruseroptions"></a>

Specifies information about the master user\.

## Syntax<a name="aws-properties-elasticsearch-domain-masteruseroptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticsearch-domain-masteruseroptions-syntax.json"></a>

```
{
  "[MasterUserARN](#cfn-elasticsearch-domain-masteruseroptions-masteruserarn)" : String,
  "[MasterUserName](#cfn-elasticsearch-domain-masteruseroptions-masterusername)" : String,
  "[MasterUserPassword](#cfn-elasticsearch-domain-masteruseroptions-masteruserpassword)" : String
}
```

### YAML<a name="aws-properties-elasticsearch-domain-masteruseroptions-syntax.yaml"></a>

```
  [MasterUserARN](#cfn-elasticsearch-domain-masteruseroptions-masteruserarn): String
  [MasterUserName](#cfn-elasticsearch-domain-masteruseroptions-masterusername): String
  [MasterUserPassword](#cfn-elasticsearch-domain-masteruseroptions-masteruserpassword): String
```

## Properties<a name="aws-properties-elasticsearch-domain-masteruseroptions-properties"></a>

`MasterUserARN`  <a name="cfn-elasticsearch-domain-masteruseroptions-masteruserarn"></a>
ARN for the master user\. Only specify if `InternalUserDatabaseEnabled` is false in `AdvancedSecurityOptions`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MasterUserName`  <a name="cfn-elasticsearch-domain-masteruseroptions-masterusername"></a>
Username for the master user\. Only specify if `InternalUserDatabaseEnabled` is true in `AdvancedSecurityOptions`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MasterUserPassword`  <a name="cfn-elasticsearch-domain-masteruseroptions-masteruserpassword"></a>
Password for the master user\. Only specify if `InternalUserDatabaseEnabled` is true in `AdvancedSecurityOptions`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)