# Amazon S3 Bucket CorsRule<a name="aws-properties-s3-bucket-cors-corsrule"></a>

Describes cross\-origin access rules for the [Amazon S3 Bucket CorsConfiguration](aws-properties-s3-bucket-cors.md) property\.

## Syntax<a name="w3ab2c21c14e1482b5"></a>

### JSON<a name="aws-properties-s3-bucket-cors-corsrule-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-s3-bucket-cors-corsrule-allowedheaders)" : [ String, ... ],
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-s3-bucket-cors-corsrule-allowedmethods)" : [ String, ... ],
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-s3-bucket-cors-corsrule-allowedorigins)" : [ String, ... ],
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-s3-bucket-cors-corsrule-exposedheaders)" : [ String, ... ],
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-s3-bucket-cors-corsrule-id)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-s3-bucket-cors-corsrule-maxage)" : Integer
}
```

### YAML<a name="aws-properties-s3-bucket-cors-corsrule-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-s3-bucket-cors-corsrule-allowedheaders):
  - String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-s3-bucket-cors-corsrule-allowedmethods):
  - String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-s3-bucket-cors-corsrule-allowedorigins):
  - String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-s3-bucket-cors-corsrule-exposedheaders):
  - String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-s3-bucket-cors-corsrule-id): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-s3-bucket-cors-corsrule-maxage): Integer
```

## Properties<a name="w3ab2c21c14e1482b7"></a>

`AllowedHeaders`  
Headers that are specified in the `Access-Control-Request-Headers` header\. These headers are allowed in a preflight OPTIONS request\. In response to any preflight OPTIONS request, Amazon S3 returns any requested headers that are allowed\.  
*Required: *No  
*Type*: List of String values

`AllowedMethods`  
An HTTP method that you allow the origin to execute\. The valid values are `GET`, `PUT`, `HEAD`, `POST`, and `DELETE`\.  
*Required: *Yes  
*Type*: List of String values

`AllowedOrigins`  
An origin that you allow to send cross\-domain requests\.  
*Required: *Yes  
*Type*: List of String values

`ExposedHeaders`  
One or more headers in the response that are accessible to client applications \(for example, from a JavaScript XMLHttpRequest object\)\.  
*Required: *No  
*Type*: List of String values

`Id`  
A unique identifier for this rule\. The value cannot be more than 255 characters\.  
*Required: *No  
*Type*: String

`MaxAge`  
The time in seconds that your browser is to cache the preflight response for the specified resource\.  
*Required: *No  
*Type*: Integer