# AWS::Lambda::Url Cors<a name="aws-properties-lambda-url-cors"></a>

The [Cross\-Origin Resource Sharing \(CORS\)](https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS) settings for your function URL\. Use CORS to grant access to your function URL from any origin\. You can also use CORS to control access for specific HTTP headers and methods in requests to your function URL\.

## Syntax<a name="aws-properties-lambda-url-cors-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lambda-url-cors-syntax.json"></a>

```
{
  "[AllowCredentials](#cfn-lambda-url-cors-allowcredentials)" : Boolean,
  "[AllowHeaders](#cfn-lambda-url-cors-allowheaders)" : [ String, ... ],
  "[AllowMethods](#cfn-lambda-url-cors-allowmethods)" : [ String, ... ],
  "[AllowOrigins](#cfn-lambda-url-cors-alloworigins)" : [ String, ... ],
  "[ExposeHeaders](#cfn-lambda-url-cors-exposeheaders)" : [ String, ... ],
  "[MaxAge](#cfn-lambda-url-cors-maxage)" : Integer
}
```

### YAML<a name="aws-properties-lambda-url-cors-syntax.yaml"></a>

```
  [AllowCredentials](#cfn-lambda-url-cors-allowcredentials): Boolean
  [AllowHeaders](#cfn-lambda-url-cors-allowheaders): 
    - String
  [AllowMethods](#cfn-lambda-url-cors-allowmethods): 
    - String
  [AllowOrigins](#cfn-lambda-url-cors-alloworigins): 
    - String
  [ExposeHeaders](#cfn-lambda-url-cors-exposeheaders): 
    - String
  [MaxAge](#cfn-lambda-url-cors-maxage): Integer
```

## Properties<a name="aws-properties-lambda-url-cors-properties"></a>

`AllowCredentials`  <a name="cfn-lambda-url-cors-allowcredentials"></a>
Whether you want to allow cookies or other credentials in requests to your function URL\. The default is `false`\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AllowHeaders`  <a name="cfn-lambda-url-cors-allowheaders"></a>
The HTTP headers that origins can include in requests to your function URL\. For example: `Date`, `Keep-Alive`, `X-Custom-Header`\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AllowMethods`  <a name="cfn-lambda-url-cors-allowmethods"></a>
The HTTP methods that are allowed when calling your function URL\. For example: `GET`, `POST`, `DELETE`, or the wildcard character \(`*`\)\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `6`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AllowOrigins`  <a name="cfn-lambda-url-cors-alloworigins"></a>
The origins that can access your function URL\. You can list any number of specific origins, separated by a comma\. For example: `https://www.example.com`, `http://localhost:60905`\.  
Alternatively, you can grant access to all origins with the wildcard character \(`*`\)\.   
*Required*: No  
*Type*: List of String  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ExposeHeaders`  <a name="cfn-lambda-url-cors-exposeheaders"></a>
The HTTP headers in your function response that you want to expose to origins that call your function URL\. For example: `Date`, `Keep-Alive`, `X-Custom-Header`\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaxAge`  <a name="cfn-lambda-url-cors-maxage"></a>
The maximum amount of time, in seconds, that browsers can cache results of a preflight request\. By default, this is set to `0`, which means the browser will not cache results\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `0`  
*Maximum*: `86400`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)