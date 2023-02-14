# AWS::MediaConnect::FlowOutput Encryption<a name="aws-properties-mediaconnect-flowoutput-encryption"></a>

Information about the encryption of the flow\.

## Syntax<a name="aws-properties-mediaconnect-flowoutput-encryption-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-mediaconnect-flowoutput-encryption-syntax.json"></a>

```
{
  "[Algorithm](#cfn-mediaconnect-flowoutput-encryption-algorithm)" : String,
  "[KeyType](#cfn-mediaconnect-flowoutput-encryption-keytype)" : String,
  "[RoleArn](#cfn-mediaconnect-flowoutput-encryption-rolearn)" : String,
  "[SecretArn](#cfn-mediaconnect-flowoutput-encryption-secretarn)" : String
}
```

### YAML<a name="aws-properties-mediaconnect-flowoutput-encryption-syntax.yaml"></a>

```
  [Algorithm](#cfn-mediaconnect-flowoutput-encryption-algorithm): String
  [KeyType](#cfn-mediaconnect-flowoutput-encryption-keytype): String
  [RoleArn](#cfn-mediaconnect-flowoutput-encryption-rolearn): String
  [SecretArn](#cfn-mediaconnect-flowoutput-encryption-secretarn): String
```

## Properties<a name="aws-properties-mediaconnect-flowoutput-encryption-properties"></a>

`Algorithm`  <a name="cfn-mediaconnect-flowoutput-encryption-algorithm"></a>
The type of algorithm that is used for the encryption \(such as aes128, aes192, or aes256\)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KeyType`  <a name="cfn-mediaconnect-flowoutput-encryption-keytype"></a>
The type of key that is used for the encryption\. If you don't specify a `keyType` value, the service uses the default setting \(`static-key`\)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleArn`  <a name="cfn-mediaconnect-flowoutput-encryption-rolearn"></a>
The Amazon Resource Name \(ARN\) of the role that you created during setup \(when you set up MediaConnect as a trusted entity\)\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecretArn`  <a name="cfn-mediaconnect-flowoutput-encryption-secretarn"></a>
The ARN of the secret that you created in AWS Secrets Manager to store the encryption key\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)