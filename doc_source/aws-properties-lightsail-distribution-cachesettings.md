# AWS::Lightsail::Distribution CacheSettings<a name="aws-properties-lightsail-distribution-cachesettings"></a>

`CacheSettings` is a property of the [AWS::Lightsail::Distribution](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-lightsail-distribution.html) resource\. It describes the cache settings of an Amazon Lightsail content delivery network \(CDN\) distribution\.

These settings apply only to your distribution’s `CacheBehaviors` that have a `Behavior` of `cache`\. This includes the `DefaultCacheBehavior`\.

## Syntax<a name="aws-properties-lightsail-distribution-cachesettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lightsail-distribution-cachesettings-syntax.json"></a>

```
{
  "[AllowedHTTPMethods](#cfn-lightsail-distribution-cachesettings-allowedhttpmethods)" : String,
  "[CachedHTTPMethods](#cfn-lightsail-distribution-cachesettings-cachedhttpmethods)" : String,
  "[DefaultTTL](#cfn-lightsail-distribution-cachesettings-defaultttl)" : Integer,
  "[ForwardedCookies](#cfn-lightsail-distribution-cachesettings-forwardedcookies)" : CookieObject,
  "[ForwardedHeaders](#cfn-lightsail-distribution-cachesettings-forwardedheaders)" : HeaderObject,
  "[ForwardedQueryStrings](#cfn-lightsail-distribution-cachesettings-forwardedquerystrings)" : QueryStringObject,
  "[MaximumTTL](#cfn-lightsail-distribution-cachesettings-maximumttl)" : Integer,
  "[MinimumTTL](#cfn-lightsail-distribution-cachesettings-minimumttl)" : Integer
}
```

### YAML<a name="aws-properties-lightsail-distribution-cachesettings-syntax.yaml"></a>

```
  [AllowedHTTPMethods](#cfn-lightsail-distribution-cachesettings-allowedhttpmethods): String
  [CachedHTTPMethods](#cfn-lightsail-distribution-cachesettings-cachedhttpmethods): String
  [DefaultTTL](#cfn-lightsail-distribution-cachesettings-defaultttl): Integer
  [ForwardedCookies](#cfn-lightsail-distribution-cachesettings-forwardedcookies): 
    CookieObject
  [ForwardedHeaders](#cfn-lightsail-distribution-cachesettings-forwardedheaders): 
    HeaderObject
  [ForwardedQueryStrings](#cfn-lightsail-distribution-cachesettings-forwardedquerystrings): 
    QueryStringObject
  [MaximumTTL](#cfn-lightsail-distribution-cachesettings-maximumttl): Integer
  [MinimumTTL](#cfn-lightsail-distribution-cachesettings-minimumttl): Integer
```

## Properties<a name="aws-properties-lightsail-distribution-cachesettings-properties"></a>

`AllowedHTTPMethods`  <a name="cfn-lightsail-distribution-cachesettings-allowedhttpmethods"></a>
The HTTP methods that are processed and forwarded to the distribution's origin\.  
You can specify the following options:  
+  `GET,HEAD` \- The distribution forwards the `GET` and `HEAD` methods\.
+  `GET,HEAD,OPTIONS` \- The distribution forwards the `GET`, `HEAD`, and `OPTIONS` methods\.
+  `GET,HEAD,OPTIONS,PUT,PATCH,POST,DELETE` \- The distribution forwards the `GET`, `HEAD`, `OPTIONS`, `PUT`, `PATCH`, `POST`, and `DELETE` methods\.
If you specify `GET,HEAD,OPTIONS,PUT,PATCH,POST,DELETE`, you might need to restrict access to your distribution's origin so users can't perform operations that you don't want them to\. For example, you might not want users to have permission to delete objects from your origin\.  
*Required*: No  
*Type*: String  
*Pattern*: `.*\S.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CachedHTTPMethods`  <a name="cfn-lightsail-distribution-cachesettings-cachedhttpmethods"></a>
The HTTP method responses that are cached by your distribution\.  
You can specify the following options:  
+  `GET,HEAD` \- The distribution caches responses to the `GET` and `HEAD` methods\.
+  `GET,HEAD,OPTIONS` \- The distribution caches responses to the `GET`, `HEAD`, and `OPTIONS` methods\.
*Required*: No  
*Type*: String  
*Pattern*: `.*\S.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DefaultTTL`  <a name="cfn-lightsail-distribution-cachesettings-defaultttl"></a>
The default amount of time that objects stay in the distribution's cache before the distribution forwards another request to the origin to determine whether the content has been updated\.  
The value specified applies only when the origin does not add HTTP headers such as `Cache-Control max-age`, `Cache-Control s-maxage`, and `Expires` to objects\.
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ForwardedCookies`  <a name="cfn-lightsail-distribution-cachesettings-forwardedcookies"></a>
An object that describes the cookies that are forwarded to the origin\. Your content is cached based on the cookies that are forwarded\.  
*Required*: No  
*Type*: [CookieObject](aws-properties-lightsail-distribution-cookieobject.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ForwardedHeaders`  <a name="cfn-lightsail-distribution-cachesettings-forwardedheaders"></a>
An object that describes the headers that are forwarded to the origin\. Your content is cached based on the headers that are forwarded\.  
*Required*: No  
*Type*: [HeaderObject](aws-properties-lightsail-distribution-headerobject.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ForwardedQueryStrings`  <a name="cfn-lightsail-distribution-cachesettings-forwardedquerystrings"></a>
An object that describes the query strings that are forwarded to the origin\. Your content is cached based on the query strings that are forwarded\.  
*Required*: No  
*Type*: [QueryStringObject](aws-properties-lightsail-distribution-querystringobject.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaximumTTL`  <a name="cfn-lightsail-distribution-cachesettings-maximumttl"></a>
The maximum amount of time that objects stay in the distribution's cache before the distribution forwards another request to the origin to determine whether the object has been updated\.  
The value specified applies only when the origin adds HTTP headers such as `Cache-Control max-age`, `Cache-Control s-maxage`, and `Expires` to objects\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MinimumTTL`  <a name="cfn-lightsail-distribution-cachesettings-minimumttl"></a>
The minimum amount of time that objects stay in the distribution's cache before the distribution forwards another request to the origin to determine whether the object has been updated\.  
A value of `0` must be specified for `minimumTTL` if the distribution is configured to forward all headers to the origin\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)