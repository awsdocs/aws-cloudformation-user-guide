# Amazon S3 Website Configuration Routing Rules Redirect Rule Property<a name="aws-properties-s3-websiteconfiguration-routingrules-redirectrule"></a>

The `RedirectRule` property is an embedded property of the [Amazon S3 Website Configuration Routing Rules Property](aws-properties-s3-websiteconfiguration-routingrules.md) that describes how requests are redirected\. In the event of an error, you can specify a different error code to return\.

## Syntax<a name="w3ab2c21c14e1818b5"></a>

### JSON<a name="aws-properties-s3-websiteconfiguration-routingrules-redirectrule-syntax.json"></a>

```
{
  "[HostName](#cfn-s3-websiteconfiguration-redirectrule-hostname)" : String,
  "[HttpRedirectCode](#cfn-s3-websiteconfiguration-redirectrule-httpredirectcode)" : String,
  "[Protocol](#cfn-s3-websiteconfiguration-redirectrule-protocol)" : String,
  "[ReplaceKeyPrefixWith](#cfn-s3-websiteconfiguration-redirectrule-replacekeyprefixwith)" : String,
  "[ReplaceKeyWith](#cfn-s3-websiteconfiguration-redirectrule-replacekeywith)" : String
}
```

### YAML<a name="aws-properties-s3-websiteconfiguration-routingrules-redirectrule-syntax.yaml"></a>

```
[HostName](#cfn-s3-websiteconfiguration-redirectrule-hostname): String
[HttpRedirectCode](#cfn-s3-websiteconfiguration-redirectrule-httpredirectcode): String
[Protocol](#cfn-s3-websiteconfiguration-redirectrule-protocol): String
[ReplaceKeyPrefixWith](#cfn-s3-websiteconfiguration-redirectrule-replacekeyprefixwith): String
[ReplaceKeyWith](#cfn-s3-websiteconfiguration-redirectrule-replacekeywith): String
```

## Properties<a name="w3ab2c21c14e1818b7"></a>

`HostName`  <a name="cfn-s3-websiteconfiguration-redirectrule-hostname"></a>
Name of the host where requests are redirected\.  
*Required*: No  
*Type*: String

`HttpRedirectCode`  <a name="cfn-s3-websiteconfiguration-redirectrule-httpredirectcode"></a>
The HTTP redirect code to use on the response\.  
*Required*: No  
*Type*: String

`Protocol`  <a name="cfn-s3-websiteconfiguration-redirectrule-protocol"></a>
The protocol to use in the redirect request\.  
*Required*: No  
*Type*: String

`ReplaceKeyPrefixWith`  <a name="cfn-s3-websiteconfiguration-redirectrule-replacekeyprefixwith"></a>
The object key prefix to use in the redirect request\. For example, to redirect requests for all pages with the prefix `docs/` \(objects in the `docs/` folder\) to the `documents/` prefix, you can set the `KeyPrefixEquals` property in routing condition property to `docs/`, and set the *ReplaceKeyPrefixWith* property to `documents/`\.  
If you specify this property, you cannot specify the `ReplaceKeyWith` property\.
*Required*: No  
*Type*: String

`ReplaceKeyWith`  <a name="cfn-s3-websiteconfiguration-redirectrule-replacekeywith"></a>
The specific object key to use in the redirect request\. For example, redirect request to `error.html`\.  
If you specify this property, you cannot specify the `ReplaceKeyPrefixWith` property\.
*Required*: No  
*Type*: String