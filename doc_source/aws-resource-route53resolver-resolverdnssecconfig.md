# AWS::Route53Resolver::ResolverDNSSECConfig<a name="aws-resource-route53resolver-resolverdnssecconfig"></a>

The `AWS::Route53Resolver::ResolverDNSSECConfig` resource is a complex type that contains information about a configuration for DNSSEC validation\.

## Syntax<a name="aws-resource-route53resolver-resolverdnssecconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-route53resolver-resolverdnssecconfig-syntax.json"></a>

```
{
  "Type" : "AWS::Route53Resolver::ResolverDNSSECConfig",
  "Properties" : {
      "[ResourceId](#cfn-route53resolver-resolverdnssecconfig-resourceid)" : String
    }
}
```

### YAML<a name="aws-resource-route53resolver-resolverdnssecconfig-syntax.yaml"></a>

```
Type: AWS::Route53Resolver::ResolverDNSSECConfig
Properties: 
  [ResourceId](#cfn-route53resolver-resolverdnssecconfig-resourceid): String
```

## Properties<a name="aws-resource-route53resolver-resolverdnssecconfig-properties"></a>

`ResourceId`  <a name="cfn-route53resolver-resolverdnssecconfig-resourceid"></a>
The ID of the virtual private cloud \(VPC\) that you're configuring the DNSSEC validation status for\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `64`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-route53resolver-resolverdnssecconfig-return-values"></a>

### Ref<a name="aws-resource-route53resolver-resolverdnssecconfig-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ID\. For example:

 `{ "Ref": "rdsc-689d45d1ae623bf3" }` 

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-route53resolver-resolverdnssecconfig-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-route53resolver-resolverdnssecconfig-return-values-fn--getatt-fn--getatt"></a>

`Id`  <a name="Id-fn::getatt"></a>
The primary identifier of this `ResolverDNSSECConfig` resource\. For example: `rdsc-689d45d1ae623bf3`\.

`OwnerId`  <a name="OwnerId-fn::getatt"></a>
The AWS account of the owner\. For example: `111122223333`\.

`ValidationStatus`  <a name="ValidationStatus-fn::getatt"></a>
The current status of this `ResolverDNSSECConfig` resource\. For example: `Enabled`\.