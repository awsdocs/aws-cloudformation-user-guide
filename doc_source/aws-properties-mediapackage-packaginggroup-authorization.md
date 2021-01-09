# AWS::MediaPackage::PackagingGroup Authorization<a name="aws-properties-mediapackage-packaginggroup-authorization"></a>

Parameters for enabling CDN authorization\.

## Syntax<a name="aws-properties-mediapackage-packaginggroup-authorization-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-mediapackage-packaginggroup-authorization-syntax.json"></a>

```
{
  "[CdnIdentifierSecret](#cfn-mediapackage-packaginggroup-authorization-cdnidentifiersecret)" : String,
  "[SecretsRoleArn](#cfn-mediapackage-packaginggroup-authorization-secretsrolearn)" : String
}
```

### YAML<a name="aws-properties-mediapackage-packaginggroup-authorization-syntax.yaml"></a>

```
  [CdnIdentifierSecret](#cfn-mediapackage-packaginggroup-authorization-cdnidentifiersecret): String
  [SecretsRoleArn](#cfn-mediapackage-packaginggroup-authorization-secretsrolearn): String
```

## Properties<a name="aws-properties-mediapackage-packaginggroup-authorization-properties"></a>

`CdnIdentifierSecret`  <a name="cfn-mediapackage-packaginggroup-authorization-cdnidentifiersecret"></a>
The Amazon Resource Name \(ARN\) for the secret in AWS Secrets Manager that is used for CDN authorization\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecretsRoleArn`  <a name="cfn-mediapackage-packaginggroup-authorization-secretsrolearn"></a>
The Amazon Resource Name \(ARN\) for the IAM role that allows MediaPackage to communicate with AWS Secrets Manager\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)