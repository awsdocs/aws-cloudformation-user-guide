# AWS::MediaPackage::OriginEndpoint Authorization<a name="aws-properties-mediapackage-originendpoint-authorization"></a>

Parameters for enabling CDN authorization on the endpoint\.

## Syntax<a name="aws-properties-mediapackage-originendpoint-authorization-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-mediapackage-originendpoint-authorization-syntax.json"></a>

```
{
  "[CdnIdentifierSecret](#cfn-mediapackage-originendpoint-authorization-cdnidentifiersecret)" : String,
  "[SecretsRoleArn](#cfn-mediapackage-originendpoint-authorization-secretsrolearn)" : String
}
```

### YAML<a name="aws-properties-mediapackage-originendpoint-authorization-syntax.yaml"></a>

```
  [CdnIdentifierSecret](#cfn-mediapackage-originendpoint-authorization-cdnidentifiersecret): String
  [SecretsRoleArn](#cfn-mediapackage-originendpoint-authorization-secretsrolearn): String
```

## Properties<a name="aws-properties-mediapackage-originendpoint-authorization-properties"></a>

`CdnIdentifierSecret`  <a name="cfn-mediapackage-originendpoint-authorization-cdnidentifiersecret"></a>
The Amazon Resource Name \(ARN\) for the secret in AWS Secrets Manager that your Content Distribution Network \(CDN\) uses for authorization to access your endpoint\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecretsRoleArn`  <a name="cfn-mediapackage-originendpoint-authorization-secretsrolearn"></a>
The Amazon Resource Name \(ARN\) for the IAM role that allows MediaPackage to communicate with AWS Secrets Manager\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)