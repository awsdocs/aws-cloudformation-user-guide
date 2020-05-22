# AWS::OpsWorks::App SslConfiguration<a name="aws-properties-opsworks-app-sslconfiguration"></a>

Describes an app's SSL configuration\.

## Syntax<a name="aws-properties-opsworks-app-sslconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-opsworks-app-sslconfiguration-syntax.json"></a>

```
{
  "[Certificate](#cfn-opsworks-app-sslconfig-certificate)" : String,
  "[Chain](#cfn-opsworks-app-sslconfig-chain)" : String,
  "[PrivateKey](#cfn-opsworks-app-sslconfig-privatekey)" : String
}
```

### YAML<a name="aws-properties-opsworks-app-sslconfiguration-syntax.yaml"></a>

```
  [Certificate](#cfn-opsworks-app-sslconfig-certificate): String
  [Chain](#cfn-opsworks-app-sslconfig-chain): String
  [PrivateKey](#cfn-opsworks-app-sslconfig-privatekey): String
```

## Properties<a name="aws-properties-opsworks-app-sslconfiguration-properties"></a>

`Certificate`  <a name="cfn-opsworks-app-sslconfig-certificate"></a>
The contents of the certificate's domain\.crt file\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Chain`  <a name="cfn-opsworks-app-sslconfig-chain"></a>
Optional\. Can be used to specify an intermediate certificate authority key or client authentication\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PrivateKey`  <a name="cfn-opsworks-app-sslconfig-privatekey"></a>
The private key; the contents of the certificate's domain\.kex file\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)