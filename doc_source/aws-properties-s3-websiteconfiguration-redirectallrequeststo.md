# Amazon S3 Website Configuration Redirect All Requests To Property<a name="aws-properties-s3-websiteconfiguration-redirectallrequeststo"></a>

The `RedirectAllRequestsTo` code is an embedded property of the [Amazon S3 Website Configuration Property](aws-properties-s3-websiteconfiguration.md) property that describes the redirect behavior of all requests to a website endpoint of an Amazon S3 bucket\.

## Syntax<a name="w3ab2c21c14e1554b5"></a>

### JSON<a name="aws-properties-s3-websiteconfiguration-redirectallrequeststo-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-s3-websiteconfiguration-redirectallrequeststo-hostname)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-s3-websiteconfiguration-redirectallrequeststo-protocol)" : String
}
```

### YAML<a name="aws-properties-s3-websiteconfiguration-redirectallrequeststo-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-s3-websiteconfiguration-redirectallrequeststo-hostname): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-s3-websiteconfiguration-redirectallrequeststo-protocol): String
```

## Properties<a name="w3ab2c21c14e1554b7"></a>

`HostName`  
Name of the host where requests are redirected\.  
*Required: *Yes  
*Type*: String

`Protocol`  
Protocol to use \(`http` or `https`\) when redirecting requests\. The default is the protocol that is used in the original request\.  
*Required: *No  
*Type*: String