# AWS::MediaTailor::SourceLocation SecretsManagerAccessTokenConfiguration<a name="aws-properties-mediatailor-sourcelocation-secretsmanageraccesstokenconfiguration"></a>

AWS Secrets Manager access token configuration parameters\. For information about Secrets Manager access token authentication, see [Working with AWS Secrets Manager access token authentication](https://docs.aws.amazon.com/mediatailor/latest/ug/channel-assembly-access-configuration-access-token.html)\.

## Syntax<a name="aws-properties-mediatailor-sourcelocation-secretsmanageraccesstokenconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-mediatailor-sourcelocation-secretsmanageraccesstokenconfiguration-syntax.json"></a>

```
{
  "[HeaderName](#cfn-mediatailor-sourcelocation-secretsmanageraccesstokenconfiguration-headername)" : String,
  "[SecretArn](#cfn-mediatailor-sourcelocation-secretsmanageraccesstokenconfiguration-secretarn)" : String,
  "[SecretStringKey](#cfn-mediatailor-sourcelocation-secretsmanageraccesstokenconfiguration-secretstringkey)" : String
}
```

### YAML<a name="aws-properties-mediatailor-sourcelocation-secretsmanageraccesstokenconfiguration-syntax.yaml"></a>

```
  [HeaderName](#cfn-mediatailor-sourcelocation-secretsmanageraccesstokenconfiguration-headername): String
  [SecretArn](#cfn-mediatailor-sourcelocation-secretsmanageraccesstokenconfiguration-secretarn): String
  [SecretStringKey](#cfn-mediatailor-sourcelocation-secretsmanageraccesstokenconfiguration-secretstringkey): 
    String
```

## Properties<a name="aws-properties-mediatailor-sourcelocation-secretsmanageraccesstokenconfiguration-properties"></a>

`HeaderName`  <a name="cfn-mediatailor-sourcelocation-secretsmanageraccesstokenconfiguration-headername"></a>
The name of the HTTP header used to supply the access token in requests to the source location\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecretArn`  <a name="cfn-mediatailor-sourcelocation-secretsmanageraccesstokenconfiguration-secretarn"></a>
The Amazon Resource Name \(ARN\) of the AWS Secrets Manager secret that contains the access token\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecretStringKey`  <a name="cfn-mediatailor-sourcelocation-secretsmanageraccesstokenconfiguration-secretstringkey"></a>
The AWS Secrets Manager [SecretString](https://docs.aws.amazon.com/secretsmanager/latest/apireference/API_CreateSecret.html#SecretsManager-CreateSecret-request-SecretString.html) key associated with the access token\. MediaTailor uses the key to look up SecretString key and value pair containing the access token\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)