# AWS::EC2::IPAMPoolCidr<a name="aws-resource-ec2-ipampoolcidr"></a>

A CIDR provisioned to an IPAM pool\.

## Syntax<a name="aws-resource-ec2-ipampoolcidr-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-ipampoolcidr-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::IPAMPoolCidr",
  "Properties" : {
      "[Cidr](#cfn-ec2-ipampoolcidr-cidr)" : String,
      "[IpamPoolId](#cfn-ec2-ipampoolcidr-ipampoolid)" : String,
      "[NetmaskLength](#cfn-ec2-ipampoolcidr-netmasklength)" : Integer
    }
}
```

### YAML<a name="aws-resource-ec2-ipampoolcidr-syntax.yaml"></a>

```
Type: AWS::EC2::IPAMPoolCidr
Properties: 
  [Cidr](#cfn-ec2-ipampoolcidr-cidr): String
  [IpamPoolId](#cfn-ec2-ipampoolcidr-ipampoolid): String
  [NetmaskLength](#cfn-ec2-ipampoolcidr-netmasklength): Integer
```

## Properties<a name="aws-resource-ec2-ipampoolcidr-properties"></a>

`Cidr`  <a name="cfn-ec2-ipampoolcidr-cidr"></a>
The CIDR provisioned to the IPAM pool\. A CIDR is a representation of an IP address and its associated network mask \(or netmask\) and refers to a range of IP addresses\. An IPv4 CIDR example is `10.24.34.0/23`\. An IPv6 CIDR example is `2001:DB8::/32`\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`IpamPoolId`  <a name="cfn-ec2-ipampoolcidr-ipampoolid"></a>
The ID of the IPAM pool\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`NetmaskLength`  <a name="cfn-ec2-ipampoolcidr-netmasklength"></a>
The netmask length of the CIDR you'd like to provision to a pool\. Can be used for provisioning Amazon\-provided IPv6 CIDRs to top\-level pools and for provisioning CIDRs to pools with source pools\. Cannot be used to provision BYOIP CIDRs to top\-level pools\. "NetmaskLength" or "Cidr" is required\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-ec2-ipampoolcidr-return-values"></a>

### Ref<a name="aws-resource-ec2-ipampoolcidr-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the IPAM pool ID and IPAM pool CIDR ID in the following format: `ipam-pool-01123456|ipam-pool-cidr-0123456`\.

### Fn::GetAtt<a name="aws-resource-ec2-ipampoolcidr-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-ec2-ipampoolcidr-return-values-fn--getatt-fn--getatt"></a>

`IpamPoolCidrId`  <a name="IpamPoolCidrId-fn::getatt"></a>
The IPAM pool CIDR ID\.

`State`  <a name="State-fn::getatt"></a>
The state of the CIDR\.