# AWS OpsWorks SslConfiguration Type<a name="aws-properties-opsworks-app-sslconfiguration"></a>

Describes an SSL configuration for the [AWS::OpsWorks::App](aws-resource-opsworks-app.md) resource type\.

## Syntax<a name="w3ab2c21c14e1387b5"></a>

### JSON<a name="aws-properties-opsworks-app-sslconfiguration-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-app-sslconfig-certificate)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-app-sslconfig-chain)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-app-sslconfig-privatekey)" : String
}
```

### YAML<a name="aws-properties-opsworks-app-sslconfiguration-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-app-sslconfig-certificate): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-app-sslconfig-chain): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-app-sslconfig-privatekey): String
```

## Properties<a name="w3ab2c21c14e1387b7"></a>

`Certificate`  
The contents of the certificate's `domain.crt` file\.  
*Required: *Yes  
*Type*: String

`Chain`  
An intermediate certificate authority key or client authentication\.  
*Required: *No  
*Type*: String

`PrivateKey`  
The private key; the contents of the certificate's `domain.kex` file\.  
*Required: *Yes  
*Type*: String