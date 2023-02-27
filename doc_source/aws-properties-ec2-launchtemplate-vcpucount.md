# AWS::EC2::LaunchTemplate VCpuCount<a name="aws-properties-ec2-launchtemplate-vcpucount"></a>

The minimum and maximum number of vCPUs\.

## Syntax<a name="aws-properties-ec2-launchtemplate-vcpucount-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-launchtemplate-vcpucount-syntax.json"></a>

```
{
  "[Max](#cfn-ec2-launchtemplate-vcpucount-max)" : Integer,
  "[Min](#cfn-ec2-launchtemplate-vcpucount-min)" : Integer
}
```

### YAML<a name="aws-properties-ec2-launchtemplate-vcpucount-syntax.yaml"></a>

```
  [Max](#cfn-ec2-launchtemplate-vcpucount-max): Integer
  [Min](#cfn-ec2-launchtemplate-vcpucount-min): Integer
```

## Properties<a name="aws-properties-ec2-launchtemplate-vcpucount-properties"></a>

`Max`  <a name="cfn-ec2-launchtemplate-vcpucount-max"></a>
The maximum number of vCPUs\. To specify no maximum limit, omit this parameter\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Min`  <a name="cfn-ec2-launchtemplate-vcpucount-min"></a>
The minimum number of vCPUs\. To specify no minimum limit, specify `0`\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)