# Amazon S3 Website Configuration Redirect All Requests To Property<a name="aws-properties-s3-websiteconfiguration-redirectallrequeststo"></a>

The `RedirectAllRequestsTo` code is an embedded property of the [Amazon S3 Website Configuration Property](aws-properties-s3-websiteconfiguration.md) property that describes the redirect behavior of all requests to a website endpoint of an Amazon S3 bucket\.

## Syntax<a name="w3ab2c21c14e1810b5"></a>

### JSON<a name="aws-properties-s3-websiteconfiguration-redirectallrequeststo-syntax.json"></a>

```
{
  "[HostName](#cfn-s3-websiteconfiguration-redirectallrequeststo-hostname)" : String,
  "[Protocol](#cfn-s3-websiteconfiguration-redirectallrequeststo-protocol)" : String
}
```

### YAML<a name="aws-properties-s3-websiteconfiguration-redirectallrequeststo-syntax.yaml"></a>

```
[HostName](#cfn-s3-websiteconfiguration-redirectallrequeststo-hostname): String
[Protocol](#cfn-s3-websiteconfiguration-redirectallrequeststo-protocol): String
```

## Properties<a name="w3ab2c21c14e1810b7"></a>

`HostName`  <a name="cfn-s3-websiteconfiguration-redirectallrequeststo-hostname"></a>
Name of the host where requests are redirected\.  
*Required*: Yes  
*Type*: String

`Protocol`  <a name="cfn-s3-websiteconfiguration-redirectallrequeststo-protocol"></a>
Protocol to use \(`http` or `https`\) when redirecting requests\. The default is the protocol that is used in the original request\.  
*Required*: No  
*Type*: String