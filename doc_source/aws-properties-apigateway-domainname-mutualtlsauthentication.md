# AWS::ApiGateway::DomainName MutualTlsAuthentication<a name="aws-properties-apigateway-domainname-mutualtlsauthentication"></a>

If specified, API Gateway performs two\-way authentication between the client and the server\. Clients must present a trusted certificate to access your API\.

## Syntax<a name="aws-properties-apigateway-domainname-mutualtlsauthentication-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-apigateway-domainname-mutualtlsauthentication-syntax.json"></a>

```
{
  "[TruststoreUri](#cfn-apigateway-domainname-mutualtlsauthentication-truststoreuri)" : String,
  "[TruststoreVersion](#cfn-apigateway-domainname-mutualtlsauthentication-truststoreversion)" : String
}
```

### YAML<a name="aws-properties-apigateway-domainname-mutualtlsauthentication-syntax.yaml"></a>

```
  [TruststoreUri](#cfn-apigateway-domainname-mutualtlsauthentication-truststoreuri): String
  [TruststoreVersion](#cfn-apigateway-domainname-mutualtlsauthentication-truststoreversion): String
```

## Properties<a name="aws-properties-apigateway-domainname-mutualtlsauthentication-properties"></a>

`TruststoreUri`  <a name="cfn-apigateway-domainname-mutualtlsauthentication-truststoreuri"></a>
An Amazon S3 URL that specifies the truststore for mutual TLS authentication, for example, `s3://bucket-name/key-name`\. The truststore can contain certificates from public or private certificate authorities\. To update the truststore, upload a new version to S3, and then update your custom domain name to use the new version\. To update the truststore, you must have permissions to access the S3 object\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TruststoreVersion`  <a name="cfn-apigateway-domainname-mutualtlsauthentication-truststoreversion"></a>
The version of the S3 object that contains your truststore\. To specify a version, you must have versioning enabled for the S3 bucket\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)