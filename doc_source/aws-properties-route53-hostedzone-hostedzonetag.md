# AWS::Route53::HostedZone HostedZoneTag<a name="aws-properties-route53-hostedzone-hostedzonetag"></a>

A complex type that contains information about a tag that you want to add or edit for the specified health check or hosted zone\.

## Syntax<a name="aws-properties-route53-hostedzone-hostedzonetag-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-route53-hostedzone-hostedzonetag-syntax.json"></a>

```
{
  "[Key](#cfn-route53-hostedzone-hostedzonetag-key)" : String,
  "[Value](#cfn-route53-hostedzone-hostedzonetag-value)" : String
}
```

### YAML<a name="aws-properties-route53-hostedzone-hostedzonetag-syntax.yaml"></a>

```
  [Key](#cfn-route53-hostedzone-hostedzonetag-key): String
  [Value](#cfn-route53-hostedzone-hostedzonetag-value): String
```

## Properties<a name="aws-properties-route53-hostedzone-hostedzonetag-properties"></a>

`Key`  <a name="cfn-route53-hostedzone-hostedzonetag-key"></a>
The value of `Key` depends on the operation that you want to perform:  
+  **Add a tag to a health check or hosted zone**: `Key` is the name that you want to give the new tag\.
+  **Edit a tag**: `Key` is the name of the tag that you want to change the `Value` for\.
+  ** Delete a key**: `Key` is the name of the tag you want to remove\.
+  **Give a name to a health check**: Edit the default `Name` tag\. In the Amazon Route 53 console, the list of your health checks includes a **Name** column that lets you see the name that you've given to each health check\.
*Required*: Yes  
*Type*: String  
*Maximum*: `128`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-route53-hostedzone-hostedzonetag-value"></a>
The value of `Value` depends on the operation that you want to perform:  
+  **Add a tag to a health check or hosted zone**: `Value` is the value that you want to give the new tag\.
+  **Edit a tag**: `Value` is the new value that you want to assign the tag\.
*Required*: Yes  
*Type*: String  
*Maximum*: `256`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-route53-hostedzone-hostedzonetag--seealso"></a>
+  [Return values](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-route53-hostedzone.html#aws-resource-route53-hostedzone-return-values) in the topic [AWS::Route53::HostedZone](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-route53-hostedzone.html) 
+  [Tag](https://docs.aws.amazon.com/Route53/latest/APIReference/API_Tag.html) in the *Amazon Route 53 API Reference*

