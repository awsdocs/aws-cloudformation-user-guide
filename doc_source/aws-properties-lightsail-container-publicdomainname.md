# AWS::Lightsail::Container PublicDomainName<a name="aws-properties-lightsail-container-publicdomainname"></a>

`PublicDomainName` is a property of the [AWS::Lightsail::Container](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-lightsail-container.html) resource\. It describes the public domain names to use with a container service, such as `example.com` and `www.example.com`\. It also describes the certificates to use with a container service\.

## Syntax<a name="aws-properties-lightsail-container-publicdomainname-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lightsail-container-publicdomainname-syntax.json"></a>

```
{
  "[CertificateName](#cfn-lightsail-container-publicdomainname-certificatename)" : String,
  "[DomainNames](#cfn-lightsail-container-publicdomainname-domainnames)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-lightsail-container-publicdomainname-syntax.yaml"></a>

```
  [CertificateName](#cfn-lightsail-container-publicdomainname-certificatename): String
  [DomainNames](#cfn-lightsail-container-publicdomainname-domainnames): 
    - String
```

## Properties<a name="aws-properties-lightsail-container-publicdomainname-properties"></a>

`CertificateName`  <a name="cfn-lightsail-container-publicdomainname-certificatename"></a>
The name of the certificate for the public domains\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DomainNames`  <a name="cfn-lightsail-container-publicdomainname-domainnames"></a>
The public domain names to use with the container service\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)