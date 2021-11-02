# AWS::EC2::LaunchTemplate NetworkInterfaceCount<a name="aws-properties-ec2-launchtemplate-networkinterfacecount"></a>

The minimum and maximum number of network interfaces\.

## Syntax<a name="aws-properties-ec2-launchtemplate-networkinterfacecount-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-launchtemplate-networkinterfacecount-syntax.json"></a>

```
{
  "[Max](#cfn-ec2-launchtemplate-networkinterfacecount-max)" : Integer,
  "[Min](#cfn-ec2-launchtemplate-networkinterfacecount-min)" : Integer
}
```

### YAML<a name="aws-properties-ec2-launchtemplate-networkinterfacecount-syntax.yaml"></a>

```
  [Max](#cfn-ec2-launchtemplate-networkinterfacecount-max): Integer
  [Min](#cfn-ec2-launchtemplate-networkinterfacecount-min): Integer
```

## Properties<a name="aws-properties-ec2-launchtemplate-networkinterfacecount-properties"></a>

`Max`  <a name="cfn-ec2-launchtemplate-networkinterfacecount-max"></a>
The maximum number of network interfaces\. To specify no maximum limit, omit this parameter\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Min`  <a name="cfn-ec2-launchtemplate-networkinterfacecount-min"></a>
The minimum number of network interfaces\. To specify no minimum limit, omit this parameter\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)