# AWS::EC2::IPAMScope<a name="aws-resource-ec2-ipamscope"></a>

In IPAM, a scope is the highest\-level container within IPAM\. An IPAM contains two default scopes\. Each scope represents the IP space for a single network\. The private scope is intended for all private IP address space\. The public scope is intended for all public IP address space\. Scopes enable you to reuse IP addresses across multiple unconnected networks without causing IP address overlap or conflict\.

For more information, see [How IPAM works](https://docs.aws.amazon.com/vpc/latest/ipam/how-it-works-ipam.html) in the *Amazon VPC IPAM User Guide*\.

## Syntax<a name="aws-resource-ec2-ipamscope-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-ipamscope-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::IPAMScope",
  "Properties" : {
      "[Description](#cfn-ec2-ipamscope-description)" : String,
      "[IpamId](#cfn-ec2-ipamscope-ipamid)" : String,
      "[Tags](#cfn-ec2-ipamscope-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-ec2-ipamscope-syntax.yaml"></a>

```
Type: AWS::EC2::IPAMScope
Properties: 
  [Description](#cfn-ec2-ipamscope-description): String
  [IpamId](#cfn-ec2-ipamscope-ipamid): String
  [Tags](#cfn-ec2-ipamscope-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-ec2-ipamscope-properties"></a>

`Description`  <a name="cfn-ec2-ipamscope-description"></a>
The description of the scope\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IpamId`  <a name="cfn-ec2-ipamscope-ipamid"></a>
The ID of the IPAM for which you're creating this scope\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-ec2-ipamscope-tags"></a>
The key/value combination of a tag assigned to the resource\. Use the tag key in the filter name and the tag value as the filter value\. For example, to find all resources that have a tag with the key `Owner` and the value `TeamA`, specify `tag:Owner` for the filter name and `TeamA` for the filter value\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-ec2-ipamscope-return-values"></a>

### Ref<a name="aws-resource-ec2-ipamscope-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the IPAM scope ID\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-ec2-ipamscope-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-ec2-ipamscope-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The ARN of the scope\.

`IpamArn`  <a name="IpamArn-fn::getatt"></a>
The ARN of an IPAM\.

`IpamScopeId`  <a name="IpamScopeId-fn::getatt"></a>
The ID of an IPAM scope\.

`IpamScopeType`  <a name="IpamScopeType-fn::getatt"></a>
The type of the scope\.

`IsDefault`  <a name="IsDefault-fn::getatt"></a>
Defines if the scope is the default scope or not\.

`PoolCount`  <a name="PoolCount-fn::getatt"></a>
The number of pools in a scope\.