# AWS::EC2::Instance EnclaveOptions<a name="aws-properties-ec2-instance-enclaveoptions"></a>

Indicates whether the instance is enabled for AWS Nitro Enclaves\.

## Syntax<a name="aws-properties-ec2-instance-enclaveoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-instance-enclaveoptions-syntax.json"></a>

```
{
  "[Enabled](#cfn-ec2-instance-enclaveoptions-enabled)" : Boolean
}
```

### YAML<a name="aws-properties-ec2-instance-enclaveoptions-syntax.yaml"></a>

```
  [Enabled](#cfn-ec2-instance-enclaveoptions-enabled): Boolean
```

## Properties<a name="aws-properties-ec2-instance-enclaveoptions-properties"></a>

`Enabled`  <a name="cfn-ec2-instance-enclaveoptions-enabled"></a>
If this parameter is set to `true`, the instance is enabled for AWS Nitro Enclaves; otherwise, it is not enabled for AWS Nitro Enclaves\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)