# Amazon S3 Website Configuration Property<a name="aws-properties-s3-websiteconfiguration"></a>

`WebsiteConfiguration` is an embedded property of the  AWS::S3::Bucket resource\.

## Syntax<a name="w3ab2c21c14e1550b5"></a>

### JSON<a name="aws-properties-s3-websiteconfiguration-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-s3-websiteconfiguration-errordocument)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-s3-websiteconfiguration-indexdocument)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-s3-websiteconfiguration-redirectallrequeststo)" : Redirect all requests rule,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-s3-websiteconfiguration-routingrules)" : [ Routing rule, ... ]
}
```

### YAML<a name="aws-properties-s3-websiteconfiguration-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-s3-websiteconfiguration-errordocument): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-s3-websiteconfiguration-indexdocument): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-s3-websiteconfiguration-redirectallrequeststo):
  Redirect all requests rule
[[ERROR] BAD/MISSING LINK TEXT](#cfn-s3-websiteconfiguration-routingrules):
  - Routing rule
```

## Properties<a name="w3ab2c21c14e1550b7"></a>

`ErrorDocument`  
The name of the error document for the website\.  
*Required: *No  
*Type*: String

`IndexDocument`  
The name of the index document for the website\.  
*Required: *Yes  
*Type*: String

`RedirectAllRequestsTo`  
The redirect behavior for every request to this bucket's website endpoint\.  
If you specify this property, you cannot specify any other property\.
*Required: *No  
*Type*: [Amazon S3 Website Configuration Redirect All Requests To Property](aws-properties-s3-websiteconfiguration-redirectallrequeststo.md)

`RoutingRules`  
Rules that define when a redirect is applied and the redirect behavior\.  
*Required: *No  
*Type*: List of [Amazon S3 Website Configuration Routing Rules Property](aws-properties-s3-websiteconfiguration-routingrules.md)

## Example<a name="w3ab2c21c14e1550b9"></a>

```
"S3Bucket" : {
   "Type" : "AWS::S3::Bucket",
   "Properties" : {
      "AccessControl" : "PublicRead",
      "WebsiteConfiguration" : {
         "IndexDocument" : "index.html",
         "ErrorDocument" : "error.html"
      }
   }
}
```

## See Also<a name="w3ab2c21c14e1550c11"></a>

+ [Custom Error Document Support](http://docs.aws.amazon.com/AmazonS3/latest/dev/CustomErrorDocSupport.html) in the *Amazon Simple Storage Service Developer Guide*

+ [Index Document Support](http://docs.aws.amazon.com/AmazonS3/latest/dev/IndexDocumentSupport.html) in the *Amazon Simple Storage Service Developer Guide*