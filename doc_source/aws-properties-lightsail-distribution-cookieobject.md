# AWS::Lightsail::Distribution CookieObject<a name="aws-properties-lightsail-distribution-cookieobject"></a>

`CookieObject` is a property of the [CacheSettings](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-lightsail-distribution-cachesettings.html) property\. It describes whether an Amazon Lightsail content delivery network \(CDN\) distribution forwards cookies to the origin and, if so, which ones\.

For the cookies that you specify, your distribution caches separate versions of the specified content based on the cookie values in viewer requests\.

## Syntax<a name="aws-properties-lightsail-distribution-cookieobject-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lightsail-distribution-cookieobject-syntax.json"></a>

```
{
  "[CookiesAllowList](#cfn-lightsail-distribution-cookieobject-cookiesallowlist)" : [ String, ... ],
  "[Option](#cfn-lightsail-distribution-cookieobject-option)" : String
}
```

### YAML<a name="aws-properties-lightsail-distribution-cookieobject-syntax.yaml"></a>

```
  [CookiesAllowList](#cfn-lightsail-distribution-cookieobject-cookiesallowlist): 
    - String
  [Option](#cfn-lightsail-distribution-cookieobject-option): String
```

## Properties<a name="aws-properties-lightsail-distribution-cookieobject-properties"></a>

`CookiesAllowList`  <a name="cfn-lightsail-distribution-cookieobject-cookiesallowlist"></a>
The specific cookies to forward to your distribution's origin\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Option`  <a name="cfn-lightsail-distribution-cookieobject-option"></a>
Specifies which cookies to forward to the distribution's origin for a cache behavior\.  
Use one of the following configurations for your distribution:  
+  ** `all` ** \- Forwards all cookies to your origin\.
+  ** `none` ** \- Doesn’t forward cookies to your origin\.
+  ** `allow-list` ** \- Forwards only the cookies that you specify using the `CookiesAllowList` parameter\.
*Required*: No  
*Type*: String  
*Allowed values*: `all | allow-list | none`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)