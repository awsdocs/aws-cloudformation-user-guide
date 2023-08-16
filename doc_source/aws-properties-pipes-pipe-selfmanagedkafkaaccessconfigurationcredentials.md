# AWS::Pipes::Pipe SelfManagedKafkaAccessConfigurationCredentials<a name="aws-properties-pipes-pipe-selfmanagedkafkaaccessconfigurationcredentials"></a>

The AWS Secrets Manager secret that stores your stream credentials\.

## Syntax<a name="aws-properties-pipes-pipe-selfmanagedkafkaaccessconfigurationcredentials-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-pipes-pipe-selfmanagedkafkaaccessconfigurationcredentials-syntax.json"></a>

```
{
  "[BasicAuth](#cfn-pipes-pipe-selfmanagedkafkaaccessconfigurationcredentials-basicauth)" : String,
  "[ClientCertificateTlsAuth](#cfn-pipes-pipe-selfmanagedkafkaaccessconfigurationcredentials-clientcertificatetlsauth)" : String,
  "[SaslScram256Auth](#cfn-pipes-pipe-selfmanagedkafkaaccessconfigurationcredentials-saslscram256auth)" : String,
  "[SaslScram512Auth](#cfn-pipes-pipe-selfmanagedkafkaaccessconfigurationcredentials-saslscram512auth)" : String
}
```

### YAML<a name="aws-properties-pipes-pipe-selfmanagedkafkaaccessconfigurationcredentials-syntax.yaml"></a>

```
  [BasicAuth](#cfn-pipes-pipe-selfmanagedkafkaaccessconfigurationcredentials-basicauth): String
  [ClientCertificateTlsAuth](#cfn-pipes-pipe-selfmanagedkafkaaccessconfigurationcredentials-clientcertificatetlsauth): String
  [SaslScram256Auth](#cfn-pipes-pipe-selfmanagedkafkaaccessconfigurationcredentials-saslscram256auth): String
  [SaslScram512Auth](#cfn-pipes-pipe-selfmanagedkafkaaccessconfigurationcredentials-saslscram512auth): String
```

## Properties<a name="aws-properties-pipes-pipe-selfmanagedkafkaaccessconfigurationcredentials-properties"></a>

`BasicAuth`  <a name="cfn-pipes-pipe-selfmanagedkafkaaccessconfigurationcredentials-basicauth"></a>
The ARN of the Secrets Manager secret\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ClientCertificateTlsAuth`  <a name="cfn-pipes-pipe-selfmanagedkafkaaccessconfigurationcredentials-clientcertificatetlsauth"></a>
The ARN of the Secrets Manager secret\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SaslScram256Auth`  <a name="cfn-pipes-pipe-selfmanagedkafkaaccessconfigurationcredentials-saslscram256auth"></a>
The ARN of the Secrets Manager secret\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SaslScram512Auth`  <a name="cfn-pipes-pipe-selfmanagedkafkaaccessconfigurationcredentials-saslscram512auth"></a>
The ARN of the Secrets Manager secret\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)