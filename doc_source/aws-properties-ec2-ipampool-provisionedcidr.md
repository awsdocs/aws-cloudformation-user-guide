# AWS::EC2::IPAMPool ProvisionedCidr<a name="aws-properties-ec2-ipampool-provisionedcidr"></a>

The CIDR provisioned to the IPAM pool\. A CIDR is a representation of an IP address and its associated network mask \(or netmask\) and refers to a range of IP addresses\. An IPv4 CIDR example is `10.24.34.0/23`\. An IPv6 CIDR example is `2001:DB8::/32`\.

**Note**  
This resource type does not allow you to provision a CIDR using the netmask length\. To provision a CIDR using netmask length, use [AWS::EC2::IPAMPoolCidr](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-ipampoolcidr.html)\. 

## Syntax<a name="aws-properties-ec2-ipampool-provisionedcidr-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-ipampool-provisionedcidr-syntax.json"></a>

```
{
  "[Cidr](#cfn-ec2-ipampool-provisionedcidr-cidr)" : String
}
```

### YAML<a name="aws-properties-ec2-ipampool-provisionedcidr-syntax.yaml"></a>

```
  [Cidr](#cfn-ec2-ipampool-provisionedcidr-cidr): String
```

## Properties<a name="aws-properties-ec2-ipampool-provisionedcidr-properties"></a>

`Cidr`  <a name="cfn-ec2-ipampool-provisionedcidr-cidr"></a>
The CIDR provisioned to the IPAM pool\. A CIDR is a representation of an IP address and its associated network mask \(or netmask\) and refers to a range of IP addresses\. An IPv4 CIDR example is `10.24.34.0/23`\. An IPv6 CIDR example is `2001:DB8::/32`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)