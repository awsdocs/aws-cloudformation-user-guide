# AWS::QuickSight::DataSource DataSourceCredentials<a name="aws-properties-quicksight-datasource-datasourcecredentials"></a>

Data source credentials\. This is a variant type structure\. For this structure to be valid, only one of the attributes can be non\-null\.

## Syntax<a name="aws-properties-quicksight-datasource-datasourcecredentials-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-datasource-datasourcecredentials-syntax.json"></a>

```
{
  "[CopySourceArn](#cfn-quicksight-datasource-datasourcecredentials-copysourcearn)" : String,
  "[CredentialPair](#cfn-quicksight-datasource-datasourcecredentials-credentialpair)" : CredentialPair
}
```

### YAML<a name="aws-properties-quicksight-datasource-datasourcecredentials-syntax.yaml"></a>

```
  [CopySourceArn](#cfn-quicksight-datasource-datasourcecredentials-copysourcearn): String
  [CredentialPair](#cfn-quicksight-datasource-datasourcecredentials-credentialpair): 
    CredentialPair
```

## Properties<a name="aws-properties-quicksight-datasource-datasourcecredentials-properties"></a>

`CopySourceArn`  <a name="cfn-quicksight-datasource-datasourcecredentials-copysourcearn"></a>
The Amazon Resource Name \(ARN\) of a data source that has the credential pair that you want to use\. When `CopySourceArn` is not null, the credential pair from the data source in the ARN is used as the credentials for the `DataSourceCredentials` structure\.  
*Required*: No  
*Type*: String  
*Pattern*: `^arn:[-a-z0-9]*:quicksight:[-a-z0-9]*:[0-9]{12}:datasource/.+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CredentialPair`  <a name="cfn-quicksight-datasource-datasourcecredentials-credentialpair"></a>
Credential pair\. For more information, see [CredentialPair](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-quicksight-datasource-datasourcecredentials.html#cfn-quicksight-datasource-datasourcecredentials-credentialpair)\.  
*Required*: No  
*Type*: [CredentialPair](aws-properties-quicksight-datasource-credentialpair.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)