# AWS::Lightsail::Distribution QueryStringObject<a name="aws-properties-lightsail-distribution-querystringobject"></a>

`QueryStringObject` is a property of the [CacheSettings](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-lightsail-distribution-cachesettings.html) property\. It describes the query string parameters that an Amazon Lightsail content delivery network \(CDN\) distribution to bases caching on\.

For the query strings that you specify, your distribution caches separate versions of the specified content based on the query string values in viewer requests\.

## Syntax<a name="aws-properties-lightsail-distribution-querystringobject-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lightsail-distribution-querystringobject-syntax.json"></a>

```
{
  "[Option](#cfn-lightsail-distribution-querystringobject-option)" : Boolean,
  "[QueryStringsAllowList](#cfn-lightsail-distribution-querystringobject-querystringsallowlist)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-lightsail-distribution-querystringobject-syntax.yaml"></a>

```
  [Option](#cfn-lightsail-distribution-querystringobject-option): Boolean
  [QueryStringsAllowList](#cfn-lightsail-distribution-querystringobject-querystringsallowlist): 
    - String
```

## Properties<a name="aws-properties-lightsail-distribution-querystringobject-properties"></a>

`Option`  <a name="cfn-lightsail-distribution-querystringobject-option"></a>
Indicates whether the distribution forwards and caches based on query strings\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`QueryStringsAllowList`  <a name="cfn-lightsail-distribution-querystringobject-querystringsallowlist"></a>
The specific query strings that the distribution forwards to the origin\.  
Your distribution caches content based on the specified query strings\.  
If the `option` parameter is true, then your distribution forwards all query strings, regardless of what you specify using the `QueryStringsAllowList` parameter\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)