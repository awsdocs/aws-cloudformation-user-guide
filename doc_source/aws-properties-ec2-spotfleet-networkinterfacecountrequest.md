# AWS::EC2::SpotFleet NetworkInterfaceCountRequest<a name="aws-properties-ec2-spotfleet-networkinterfacecountrequest"></a>

The minimum and maximum number of network interfaces\.

## Syntax<a name="aws-properties-ec2-spotfleet-networkinterfacecountrequest-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-spotfleet-networkinterfacecountrequest-syntax.json"></a>

```
{
  "[Max](#cfn-ec2-spotfleet-networkinterfacecountrequest-max)" : Integer,
  "[Min](#cfn-ec2-spotfleet-networkinterfacecountrequest-min)" : Integer
}
```

### YAML<a name="aws-properties-ec2-spotfleet-networkinterfacecountrequest-syntax.yaml"></a>

```
  [Max](#cfn-ec2-spotfleet-networkinterfacecountrequest-max): Integer
  [Min](#cfn-ec2-spotfleet-networkinterfacecountrequest-min): Integer
```

## Properties<a name="aws-properties-ec2-spotfleet-networkinterfacecountrequest-properties"></a>

`Max`  <a name="cfn-ec2-spotfleet-networkinterfacecountrequest-max"></a>
The maximum number of network interfaces\. To specify no maximum limit, omit this parameter\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Min`  <a name="cfn-ec2-spotfleet-networkinterfacecountrequest-min"></a>
The minimum number of network interfaces\. To specify no minimum limit, omit this parameter\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)