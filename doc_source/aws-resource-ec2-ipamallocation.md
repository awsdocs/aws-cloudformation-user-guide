# AWS::EC2::IPAMAllocation<a name="aws-resource-ec2-ipamallocation"></a>

In IPAM, an allocation is a CIDR assignment from an IPAM pool to another IPAM pool or to a resource\.

## Syntax<a name="aws-resource-ec2-ipamallocation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-ipamallocation-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::IPAMAllocation",
  "Properties" : {
      "[Cidr](#cfn-ec2-ipamallocation-cidr)" : String,
      "[Description](#cfn-ec2-ipamallocation-description)" : String,
      "[IpamPoolId](#cfn-ec2-ipamallocation-ipampoolid)" : String,
      "[NetmaskLength](#cfn-ec2-ipamallocation-netmasklength)" : Integer
    }
}
```

### YAML<a name="aws-resource-ec2-ipamallocation-syntax.yaml"></a>

```
Type: AWS::EC2::IPAMAllocation
Properties: 
  [Cidr](#cfn-ec2-ipamallocation-cidr): String
  [Description](#cfn-ec2-ipamallocation-description): String
  [IpamPoolId](#cfn-ec2-ipamallocation-ipampoolid): String
  [NetmaskLength](#cfn-ec2-ipamallocation-netmasklength): Integer
```

## Properties<a name="aws-resource-ec2-ipamallocation-properties"></a>

`Cidr`  <a name="cfn-ec2-ipamallocation-cidr"></a>
The CIDR you would like to allocate from the IPAM pool\. Note the following:  
+ If there is no DefaultNetmaskLength allocation rule set on the pool, you must specify either the NetmaskLength or the CIDR\.
+ If the DefaultNetmaskLength allocation rule is set on the pool, you can specify either the NetmaskLength or the CIDR and the DefaultNetmaskLength allocation rule will be ignored\.
Possible values: Any available IPv4 or IPv6 CIDR\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Description`  <a name="cfn-ec2-ipamallocation-description"></a>
A description for the allocation\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`IpamPoolId`  <a name="cfn-ec2-ipamallocation-ipampoolid"></a>
The ID of the IPAM pool from which you would like to allocate a CIDR\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`NetmaskLength`  <a name="cfn-ec2-ipamallocation-netmasklength"></a>
The netmask length of the CIDR you would like to allocate from the IPAM pool\. Note the following:  
+ If there is no DefaultNetmaskLength allocation rule set on the pool, you must specify either the NetmaskLength or the CIDR\.
+ If the DefaultNetmaskLength allocation rule is set on the pool, you can specify either the NetmaskLength or the CIDR and the DefaultNetmaskLength allocation rule will be ignored\.
Possible netmask lengths for IPv4 addresses are 0 \- 32\. Possible netmask lengths for IPv6 addresses are 0 \- 128\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-ec2-ipamallocation-return-values"></a>

### Ref<a name="aws-resource-ec2-ipamallocation-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the pool ID, allocation ID, and CIDR\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-ec2-ipamallocation-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-ec2-ipamallocation-return-values-fn--getatt-fn--getatt"></a>

`IpamPoolAllocationId`  <a name="IpamPoolAllocationId-fn::getatt"></a>
The ID of an allocation\.