# AWS::EC2::VerifiedAccessEndpoint NetworkInterfaceOptions<a name="aws-properties-ec2-verifiedaccessendpoint-networkinterfaceoptions"></a>

Describes the network interface options when creating an AWS Verified Access endpoint using the `network-interface` type\.

## Syntax<a name="aws-properties-ec2-verifiedaccessendpoint-networkinterfaceoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-verifiedaccessendpoint-networkinterfaceoptions-syntax.json"></a>

```
{
  "[NetworkInterfaceId](#cfn-ec2-verifiedaccessendpoint-networkinterfaceoptions-networkinterfaceid)" : String,
  "[Port](#cfn-ec2-verifiedaccessendpoint-networkinterfaceoptions-port)" : Integer,
  "[Protocol](#cfn-ec2-verifiedaccessendpoint-networkinterfaceoptions-protocol)" : String
}
```

### YAML<a name="aws-properties-ec2-verifiedaccessendpoint-networkinterfaceoptions-syntax.yaml"></a>

```
  [NetworkInterfaceId](#cfn-ec2-verifiedaccessendpoint-networkinterfaceoptions-networkinterfaceid): String
  [Port](#cfn-ec2-verifiedaccessendpoint-networkinterfaceoptions-port): Integer
  [Protocol](#cfn-ec2-verifiedaccessendpoint-networkinterfaceoptions-protocol): String
```

## Properties<a name="aws-properties-ec2-verifiedaccessendpoint-networkinterfaceoptions-properties"></a>

`NetworkInterfaceId`  <a name="cfn-ec2-verifiedaccessendpoint-networkinterfaceoptions-networkinterfaceid"></a>
The ID of the network interface\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Port`  <a name="cfn-ec2-verifiedaccessendpoint-networkinterfaceoptions-port"></a>
The IP port number\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `1`  
*Maximum*: `65535`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Protocol`  <a name="cfn-ec2-verifiedaccessendpoint-networkinterfaceoptions-protocol"></a>
The IP protocol\.  
*Required*: No  
*Type*: String  
*Allowed values*: `http | https`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)