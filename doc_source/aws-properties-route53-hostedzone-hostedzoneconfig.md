# AWS::Route53::HostedZone HostedZoneConfig<a name="aws-properties-route53-hostedzone-hostedzoneconfig"></a>

A complex type that contains an optional comment about your hosted zone\. If you don't want to specify a comment, omit both the `HostedZoneConfig` and `Comment` elements\.

## Syntax<a name="aws-properties-route53-hostedzone-hostedzoneconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-route53-hostedzone-hostedzoneconfig-syntax.json"></a>

```
{
  "[Comment](#cfn-route53-hostedzone-hostedzoneconfig-comment)" : String
}
```

### YAML<a name="aws-properties-route53-hostedzone-hostedzoneconfig-syntax.yaml"></a>

```
﻿  [Comment](#cfn-route53-hostedzone-hostedzoneconfig-comment) : String
```

## Properties<a name="aws-properties-route53-hostedzone-hostedzoneconfig-properties"></a>

`Comment`  <a name="cfn-route53-hostedzone-hostedzoneconfig-comment"></a>
Any comments that you want to include about the hosted zone\.  
*Required*: No  
*Type*: String  
*Maximum*: `256`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See Also<a name="aws-properties-route53-hostedzone-hostedzoneconfig--seealso"></a>
+  [HostedZoneConfig](https://docs.aws.amazon.com/Route53/latest/APIReference/API_HostedZoneConfig.html) in the *Amazon Route 53 API Reference*