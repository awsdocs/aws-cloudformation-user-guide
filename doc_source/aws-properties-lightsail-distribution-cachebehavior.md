# AWS::Lightsail::Distribution CacheBehavior<a name="aws-properties-lightsail-distribution-cachebehavior"></a>

`CacheBehavior` is a property of the [AWS::Lightsail::Distribution](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-lightsail-distribution.html) resource\. It describes the default cache behavior of an Amazon Lightsail content delivery network \(CDN\) distribution\.

## Syntax<a name="aws-properties-lightsail-distribution-cachebehavior-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lightsail-distribution-cachebehavior-syntax.json"></a>

```
{
  "[Behavior](#cfn-lightsail-distribution-cachebehavior-behavior)" : String
}
```

### YAML<a name="aws-properties-lightsail-distribution-cachebehavior-syntax.yaml"></a>

```
  [Behavior](#cfn-lightsail-distribution-cachebehavior-behavior): String
```

## Properties<a name="aws-properties-lightsail-distribution-cachebehavior-properties"></a>

`Behavior`  <a name="cfn-lightsail-distribution-cachebehavior-behavior"></a>
The cache behavior of the distribution\.  
The following cache behaviors can be specified:  
+  ** `cache` ** \- This option is best for static sites\. When specified, your distribution caches and serves your entire website as static content\. This behavior is ideal for websites with static content that doesn't change depending on who views it, or for websites that don't use cookies, headers, or query strings to personalize content\.
+  ** `dont-cache` ** \- This option is best for sites that serve a mix of static and dynamic content\. When specified, your distribution caches and serves only the content that is specified in the distribution’s `CacheBehaviorPerPath` parameter\. This behavior is ideal for websites or web applications that use cookies, headers, and query strings to personalize content for individual users\.
*Required*: No  
*Type*: String  
*Allowed values*: `cache | dont-cache`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)