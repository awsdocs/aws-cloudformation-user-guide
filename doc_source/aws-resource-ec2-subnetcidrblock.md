# AWS::EC2::SubnetCidrBlock<a name="aws-resource-ec2-subnetcidrblock"></a>

Associates a CIDR block with your subnet\. You can associate a single IPv6 CIDR block with your subnet\. An IPv6 CIDR block must have a prefix length of /64\.

## Syntax<a name="aws-resource-ec2-subnetcidrblock-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-subnetcidrblock-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::SubnetCidrBlock",
  "Properties" : {
      "[Ipv6CidrBlock](#cfn-ec2-subnetcidrblock-ipv6cidrblock)" : String,
      "[SubnetId](#cfn-ec2-subnetcidrblock-subnetid)" : String
    }
}
```

### YAML<a name="aws-resource-ec2-subnetcidrblock-syntax.yaml"></a>

```
Type: AWS::EC2::SubnetCidrBlock
Properties: 
  [Ipv6CidrBlock](#cfn-ec2-subnetcidrblock-ipv6cidrblock): String
  [SubnetId](#cfn-ec2-subnetcidrblock-subnetid): String
```

## Properties<a name="aws-resource-ec2-subnetcidrblock-properties"></a>

`Ipv6CidrBlock`  <a name="cfn-ec2-subnetcidrblock-ipv6cidrblock"></a>
The IPv6 network range for the subnet, in CIDR notation\. The subnet size must use a /64 prefix length\.  
This parameter is required for an IPv6 only subnet\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SubnetId`  <a name="cfn-ec2-subnetcidrblock-subnetid"></a>
The ID of the subnet\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-ec2-subnetcidrblock-return-values"></a>

### Ref<a name="aws-resource-ec2-subnetcidrblock-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the association ID for the subnet’s IPv6 CIDR block\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.