# AWS::Lightsail::Distribution HeaderObject<a name="aws-properties-lightsail-distribution-headerobject"></a>

`HeaderObject` is a property of the [CacheSettings](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-lightsail-distribution-cachesettings.html) property\. It describes the request headers used by your distribution, which caches your content based on the request headers\.

For the headers that you specify, your distribution caches separate versions of the specified content based on the header values in viewer requests\. For example, suppose that viewer requests for logo\.jpg contain a custom product header that has a value of either acme or apex\. Also, suppose that you configure your distribution to cache your content based on values in the product header\. Your distribution forwards the product header to the origin and caches the response from the origin once for each header value\.

## Syntax<a name="aws-properties-lightsail-distribution-headerobject-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lightsail-distribution-headerobject-syntax.json"></a>

```
{
  "[HeadersAllowList](#cfn-lightsail-distribution-headerobject-headersallowlist)" : [ String, ... ],
  "[Option](#cfn-lightsail-distribution-headerobject-option)" : String
}
```

### YAML<a name="aws-properties-lightsail-distribution-headerobject-syntax.yaml"></a>

```
  [HeadersAllowList](#cfn-lightsail-distribution-headerobject-headersallowlist): 
    - String
  [Option](#cfn-lightsail-distribution-headerobject-option): String
```

## Properties<a name="aws-properties-lightsail-distribution-headerobject-properties"></a>

`HeadersAllowList`  <a name="cfn-lightsail-distribution-headerobject-headersallowlist"></a>
The specific headers to forward to your distribution's origin\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Option`  <a name="cfn-lightsail-distribution-headerobject-option"></a>
The headers that you want your distribution to forward to your origin\. Your distribution caches your content based on these headers\.  
Use one of the following configurations for your distribution:  
+  ** `all` ** \- Forwards all headers to your origin\.\.
+  ** `none` ** \- Forwards only the default headers\.
+  ** `allow-list` ** \- Forwards only the headers that you specify using the `HeadersAllowList` parameter\.
*Required*: No  
*Type*: String  
*Allowed values*: `all | allow-list | none`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)