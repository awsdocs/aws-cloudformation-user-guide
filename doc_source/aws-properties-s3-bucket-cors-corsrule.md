# AWS::S3::Bucket CorsRule<a name="aws-properties-s3-bucket-cors-corsrule"></a>

Specifies a cross\-origin access rule for an Amazon S3 bucket\.

## Syntax<a name="aws-properties-s3-bucket-cors-corsrule-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3-bucket-cors-corsrule-syntax.json"></a>

```
{
  "[AllowedHeaders](#cfn-s3-bucket-cors-corsrule-allowedheaders)" : [ String, ... ],
  "[AllowedMethods](#cfn-s3-bucket-cors-corsrule-allowedmethods)" : [ String, ... ],
  "[AllowedOrigins](#cfn-s3-bucket-cors-corsrule-allowedorigins)" : [ String, ... ],
  "[ExposedHeaders](#cfn-s3-bucket-cors-corsrule-exposedheaders)" : [ String, ... ],
  "[Id](#cfn-s3-bucket-cors-corsrule-id)" : String,
  "[MaxAge](#cfn-s3-bucket-cors-corsrule-maxage)" : Integer
}
```

### YAML<a name="aws-properties-s3-bucket-cors-corsrule-syntax.yaml"></a>

```
  [AllowedHeaders](#cfn-s3-bucket-cors-corsrule-allowedheaders): 
    - String
  [AllowedMethods](#cfn-s3-bucket-cors-corsrule-allowedmethods): 
    - String
  [AllowedOrigins](#cfn-s3-bucket-cors-corsrule-allowedorigins): 
    - String
  [ExposedHeaders](#cfn-s3-bucket-cors-corsrule-exposedheaders): 
    - String
  [Id](#cfn-s3-bucket-cors-corsrule-id): String
  [MaxAge](#cfn-s3-bucket-cors-corsrule-maxage): Integer
```

## Properties<a name="aws-properties-s3-bucket-cors-corsrule-properties"></a>

`AllowedHeaders`  <a name="cfn-s3-bucket-cors-corsrule-allowedheaders"></a>
Headers that are specified in the `Access-Control-Request-Headers` header\. These headers are allowed in a preflight OPTIONS request\. In response to any preflight OPTIONS request, Amazon S3 returns any requested headers that are allowed\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AllowedMethods`  <a name="cfn-s3-bucket-cors-corsrule-allowedmethods"></a>
An HTTP method that you allow the origin to run\. Valid values are `GET`, `PUT`, `HEAD`, `POST`, and `DELETE`\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AllowedOrigins`  <a name="cfn-s3-bucket-cors-corsrule-allowedorigins"></a>
One or more origins you want customers to be able to access the bucket from\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ExposedHeaders`  <a name="cfn-s3-bucket-cors-corsrule-exposedheaders"></a>
One or more headers in the response that you want customers to be able to access from their applications \(for example, from a JavaScript `XMLHttpRequest` object\)\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Id`  <a name="cfn-s3-bucket-cors-corsrule-id"></a>
A unique identifier for this rule\. The value must be no more than 255 characters\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaxAge`  <a name="cfn-s3-bucket-cors-corsrule-maxage"></a>
The time in seconds that your browser is to cache the preflight response for the specified resource\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-s3-bucket-cors-corsrule--seealso"></a>
+ AWS::S3::Bucket [Examples](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-s3-bucket.html#aws-properties-s3-bucket--examples)

