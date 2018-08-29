# AWS OpsWorks SslConfiguration Type<a name="aws-properties-opsworks-app-sslconfiguration"></a>

Describes an SSL configuration for the [AWS::OpsWorks::App](aws-resource-opsworks-app.md) resource type\.

## Syntax<a name="w3ab2c21c14e1593b5"></a>

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

## Properties<a name="w3ab2c21c14e1593b7"></a>

`Certificate`  <a name="cfn-opsworks-app-sslconfig-certificate"></a>
The contents of the certificate's `domain.crt` file\.  
*Required*: Yes  
*Type*: String

`Chain`  <a name="cfn-opsworks-app-sslconfig-chain"></a>
An intermediate certificate authority key or client authentication\.  
*Required*: No  
*Type*: String

`PrivateKey`  <a name="cfn-opsworks-app-sslconfig-privatekey"></a>
The private key; the contents of the certificate's `domain.kex` file\.  
*Required*: Yes  
*Type*: String